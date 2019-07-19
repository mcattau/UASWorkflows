Flight Planning
===============

This document is a working guide for planning missions with UAS for
field expeditions for forest ecological applications, including site
selection and planning missions with Map Pilot

Site selection
--------------

1.  Check land ownership/management

-   In general, allowed (but always check) in National Forests, private
    property, prohibited in National Parks and Wilderness Areas, Mixed
    in State parks
-   Boulder property info:
    <a href="http://maps.boco.solutions/propertysearch/" class="uri">http://maps.boco.solutions/propertysearch/</a>
-   City OSMP:
    <a href="https://www-static.bouldercolorado.gov/docs/osmp-property-map-1-201608011355.pdf?_ga=2.49882414.940818418.1559237499-1392471265.1559089502" class="uri">https://www-static.bouldercolorado.gov/docs/osmp-property-map-1-201608011355.pdf?_ga=2.49882414.940818418.1559237499-1392471265.1559089502</a>
-   County Parks and Open space:
    -   Interactive:
        <a href="https://www.bouldercounty.org/open-space/maps/interactive-map" class="uri">https://www.bouldercounty.org/open-space/maps/interactive-map</a>
    -   PDF:
        <a href="https://assets.bouldercounty.org/wp-content/uploads/2017/03/bccp-map-open-space-current.pdf" class="uri">https://assets.bouldercounty.org/wp-content/uploads/2017/03/bccp-map-open-space-current.pdf</a>
    -   Property data:
        <a href="http://maps.boco.solutions/propertysearch/" class="uri">http://maps.boco.solutions/propertysearch/</a>
-   LiDAR data:
    <a href="http://opentopo.sdsc.edu/datasets" class="uri">http://opentopo.sdsc.edu/datasets</a>

1.  Obtain any necessary permissions
2.  Create kmls of AOIs
3.  Plan the missions with Map Pilot

Creating a new mission in Map Pilot
-----------------------------------

After opening Map Pilot  
1. Open New Mission menu item  
2. Navigate to where the flight will take place  
- You can import a .kml file to help you locate your AOI. Email the .kml
to yourself, click on the attachment, tap share icon, tap Map Pilot icon
(Map Pilot has to be open for this to work). This saves the .kml to your
file manager in Map Pilot  
3. Double tap to mark the estimated home point (i.e., launch and land
location)  
4. Tap and hold to create bounding box nodes around the survey area (it
will let you mark 3 nodes and 3 nodes only and will place an additional
nodes in between the ones you’ve designated). Hold and drag existing
nodes to move them. Single tap to remove a node  
5. The program will automatically generate a flight plan  
6. Use two-finger rotation to align the flight path perpendicular to the
wind and / or parallel to changes in topography  
7. Open Options pullout menu (top)  
- Click terrain awareness -&gt; profile to see terrain changes (tap plot
to turn on and off terrain plot). Will show up with orange light if
enabled. Terrain awareness allows for a consistent GSD despite terrain
changes. Trace finger along profile and you’ll see a corresponding blue
dot along the flight path. Review the profile to make sure it makes
sense! Saving the mission while in service (with Terrain Awareness
enabled?) will cache the terrain data as well.  
- Note: This uses specially formatted SRTM data at 30m res from 2000
between 60N and 56S latitudes. It’s coarse and will miss things &lt;30m
res and/or appearing after 2000.  
- Note: Won’t interfere with sensor-based obstacle avoidance  
- Note: Terrain aware flights set RTH to 40m above highest altitude
encountered in current flight path (no matter where it is in flight) so
that the drone doesn’t run into anything when returning to home. Watch
out for FAA regs: max flight should be 121m. For example, if flight
altitude is set for 50m , there is a 100m terrain change, and Terrain
Awareness is enabled, your RTH height will only be 90m above the tallest
point, but 190m above the lowest point, putting you above 121 m at your
lower points. Also think about offset on top of that. The UAS allows for
takeoff with a flightplan max &lt;500m (you can change this in DJI Go
settings), but this is way above FAA regs. If returning to home is part
of completed program mission, the aircraft won’t jump up 40m above max
height. It would, for example, with multibattery missions.  
- Can change the flight path between norm, grid, and lines  
- Specify overlap (90-95% for forests)  
- Max speed – leave at 15 m/s. User can set max speed, but max speed of
mission is calculated based on other parameters. Lower flight altitudes,
higher overlap, and lower light conditions require slower movement (it’s
limited by how quickly pics can be taken and stored).  
- Set max time or battery limited. If time, drone will return to home
and land close to that time. If battery limited, will return to home
with low battery.  
- Offset. You would use this if you were taking off / landing higher or
lower than your mapping plane. This adds to / subtracts from the
altitude selected in the Altitude Adjustment pullout menu below. For
example, if you wanted to have the pixel size you specified in the
Altitude Adjustment pullout menu at the top of the canopy, you would
increase the offset value to the average height of those trees. If trees
are on average 10m high, you would specify a 10m offset. Works with
Terrain Awareness. - Note: flight below takeoff level is hard to
maintain RC link (e.g., when flying down into a canyon). - Note: Don’t
fly up and over things. This might violate rule of sight for VO, but
also Map Pilot wasn’t designed for this so can lose signal.

1.  Open Flight Plan Status pullout menu (top left) to see flight
    metrics.

2.  Open Altitude Adjustment pullout menu (next one down) to change
    flight altitude / pixel resolution. FAA allows you to fly up to 400
    feet, or 121 meters. Try for 5cm/px resolution (2 inches).

3.  Open Map control pullout (next one down) to change the units and to
    save the mission (left button)

Editing, deleting, or recalling an existing mission in Map Pilot
----------------------------------------------------------------

1.  Go to Mission Management menu item
2.  Delete or change the name of an existing mission by swiping right on
    the mission of interest and selecting edit or delete
3.  If you want to edit a mission, select the mission of interest
4.  Unlock it (top left icon in a saved mission)
5.  Make any adjustments
6.  Save

-   Note: If you edit an existing mission and save it, it saves as a new
    mission with a new name (changes will not be saved unless you save
    the mission as a new mission). In other words, you can’t update an
    existing mission; rather, you create a new one.

### Look into

-   Active Connect – Connectionless uses distance aircraft has traveled
    to trigger camera rather than ?. Connectionless will still take
    pictures if the aircraft loses connection with the rc, but the
    pictures will likeluy be less uniform throughout the mission.
-   Does a flight plan buffer your AOI and by how much?
-   Are flight metrics attached to model of drone? The overlap isn’t
    sensor specific, so how does this work with different FOVs?
-   Trash can icon prob deletes mission
-   Do you need to have terrain awareness enabled to cache the SRTM data
    when you save a mission, or is the SRTM data cached anytime you save
    a mission?
-   More here:
    <a href="https://support.dronesmadeeasy.com/hc/en-us/categories/200739936-Map-Pilot-for-DJI" class="uri">https://support.dronesmadeeasy.com/hc/en-us/categories/200739936-Map-Pilot-for-DJI</a>
    and here:
    <a href="https://support.dronesmadeeasy.com/hc/en-us/community/topics" class="uri">https://support.dronesmadeeasy.com/hc/en-us/community/topics</a>
-   Can you also import geoTiff or other in addition to kml? :
    <a href="https://support.dronesmadeeasy.com/hc/en-us/articles/115000168726-3rd-Party-Basemap-Mapbox-Share-URL" class="uri">https://support.dronesmadeeasy.com/hc/en-us/articles/115000168726-3rd-Party-Basemap-Mapbox-Share-URL</a>
-   Ability to import custom DEMs instead of SRTM:
    <a href="https://support.dronesmadeeasy.com/hc/en-us/community/posts/360043459091-Terrain-Awreness" class="uri">https://support.dronesmadeeasy.com/hc/en-us/community/posts/360043459091-Terrain-Awreness</a>

Prepare for a mission in Map Pilot
----------------------------------

1.  You can simulate a flight:
    <a href="https://support.dronesmadeeasy.com/hc/en-us/articles/211468103-In-App-Simulator" class="uri">https://support.dronesmadeeasy.com/hc/en-us/articles/211468103-In-App-Simulator</a>.
    Can try in airplane mode to make sure it will work in the wilderness

Executing a Mission in Map Pilot
--------------------------------

1.  See mission checklist document
2.  Once everything on that list is completed…open MapPilot
3.  Select your saved mission from the Mission Management menu item
4.  Wait for aircraft to connect to program
5.  Check that everything looks correct in your flight and make sure
    flight lines still perpendicular to wind direction if relevant
6.  Open Flight Control pullout menu (airplane icon at top right)
7.  Upload flight plan to aircraft
8.  Check that everything is ok with the light blue line on the screen
9.  Check that the home point was set properly
10. If Terrain Awareness is enabled you’ll be prompted to select yes or
    no for a terrain adjusted flight. The profile will be recalculated,
    and you can accept or reject it after you’ve reviewed it. Note: you
    can check the profile and where the aircraft is along the profile
    during a flight, which won’t recalculate the profile
11. Set up your screen how you’d like (e.g., minimize terrain plot and
    pull up the camera)
12. Press Start
13. The UAS will fly to the start point, collect images along the flight
    path (leaving grey dots where images are selected, and the dot
    graphics are automatically cleaned as more images are collected),
    and fly to the homepoint after reaching the end point or after the
    battery drains too low (lands with juice left between 15 and 25%).
14. The UAS will automatically complete the mission, but be ready to
    land manually. It works well to swivel the camera so that it’s
    facing the same direction as the pilot (battery lights facing pilot)
    when it’s hovering above home. This makes it easier to nudge into
    place.

-   Note: Map Pilot will change the speed of the aircraft for wind and
    light conditions.
-   Note: multibattery missions. A point of abandonment is recorded when
    the drone returns to home (low battery or commanded home). Leave the
    RC on and map pilot open, change the battery, and repeat steps 6-12
    above. The UAS will return to that point of abandonment when
    commanded to go again.
