# CASE 01 · THE VANISHING ASTRONOMER

## Day 9: So Close, Yet So Far

**Difficulty:** Hard

> **CHALLENGE**
>
> You can tell you just missed her, and you're on the right trail by the map she left behind and the fire that looked hastily put out and was still slightly smoking. She circled 3 different locations, could that give a clue as to where she is going?

## Three pins, no explanation

The camp was still warm. A map left behind had three locations circled, each one labelled with nothing but a coordinate pair, scattered across Alabama and into Georgia with no line connecting them and no obvious order.

<p align="center"><img src="media-files/day09/map_three_circled_locations.png" width="500" alt="Map found at the campsite with three circled locations"></p>

<p align="center"><em>The map found at the campsite. Three points, no explanation.</em></p>

```
P1: 30.43, -88.13         |     P2: 34.80, -85.62            |     P3: 33.32, -85.00
```

## What didn't work

Most of the time on this one went nowhere, and it's worth naming the dead ends rather than pretending the answer arrived cleanly. Treated the three points as the vertices of a triangle and worked through every named centre a triangle actually has: the plain average, the point equidistant from all three corners, the point where the three altitudes cross, the point weighted by the triangle's own side lengths. Also tried matching the raw points against real places directly, observatories, state parks, dark-sky sites, on the theory that Dr. Reed would be drawn toward somewhere she could actually observe from.

A few of these landed suspiciously close to a real, named location. None of them held up under a proper distance check. Close to something real turned out to be its own trap, a coincidence dressed up as a lead.

## Why flat averaging is the wrong tool

Latitude and longitude look like ordinary x and y coordinates, so it's tempting to average three of them the obvious way: add the latitudes, add the longitudes, divide by three. That works fine near the equator, and fails a little more the further you get from it, because lines of longitude aren't evenly spaced on the ground. They squeeze together as they climb toward the poles. A degree of longitude at 35 degrees north covers noticeably less real distance than a degree of longitude at the equator. Treat every degree as equal width and the average quietly drifts off from where the three points would actually balance on a globe.

The following approach accounts for that directly: stop treating latitude and longitude as flat coordinates at all, and instead place each point in true three-dimensional space, on the surface of a sphere, then average the three points as vectors.

## Step 1: convert each point to a 3D vector

Every point on a sphere of radius 1 can be written as an (x, y, z) position using the standard conversion, with latitude and longitude first converted from degrees to radians:

```
x = cos(lat) . cos(lon)           y = cos(lat) . sin(lon)              z = sin(lat)
```

| Point | Latitude, Longitude | x | y | z |
|---|---|---|---|---|
| P1 | 30.43, -88.13 | 0.028137 | -0.861789 | 0.506485 |
| P2 | 34.80, -85.62 | 0.062712 | -0.818751 | 0.570714 |
| P3 | 33.32, -85.00 | 0.072829 | -0.832436 | 0.549315 |

## Step 2: average the three vectors

With all three points expressed in the same coordinate space, an ordinary component-wise average now means something geometrically real: add the x-values, add the y-values, add the z-values, divide each sum by three.

```
Average vector = (0.054559, -0.837659, 0.542171)
```

Checking the length of that averaged vector gives 0.999299, not exactly 1. That's expected, and it's actually the tell that this method is working correctly. Three unit vectors pointing in slightly different directions average to something a little shorter than 1, pulled inward toward the centre of the sphere, the same way the midpoint of two points on a circle's edge sits slightly inside the circle rather than on it.

## Step 3: push the point back onto the surface

Divide the averaged vector by its own length to stretch it back out to length 1, back onto the sphere's actual surface:

```
Normalised vector = (0.054597, -0.838247, 0.542551), length = 1.000000
```

## Step 4: convert back to latitude and longitude

Reverse the original conversion to read the result back off as a normal coordinate pair:

```
lat = arcsin(z)          lon = atan2(y, x)
```

That gives 32.8575, -86.2734.

## Checking it against the naive answer

Worth confirming the extra steps actually mattered rather than just trusting the method on faith. A plain flat average of the same three points, latitude and longitude added and divided by three with no spherical correction at all, gives 32.8500, -86.2500, a few kilometres away from the properly-computed point. Small on a map of the whole state, large enough to be the entire difference between a correct submission and a rejected one. That gap is exactly the distortion described above, longitude lines compressing at this latitude, made visible in the numbers rather than just argued for in the abstract.

> **FLAG**
>
> `32.8575, -86.2734`
