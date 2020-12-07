nouns: user, bike, docking station
verb: dock, view, release

User stories:
1. As a person, so that i can ride a bike, i want to view available and working bikes
2. As a person, so that i can use a working bike, i would like the docking station to release a bike
3. As a person, so that i can put back a bike, i would like the docking station to receive the bikes when space is available
4. As a user, so i can find customers, i want to search for my customers by their surnames

1.
|object| messages|
-----------------
|person| view_a_bike|
|bike| available_bike|
|docking station|

**person** -> *view_a_bike* -> *available_bike?* -> *true/false*

2.
|object| messages|
-----------------
|person| use_a_bike|
|bike| available_bike|
|docking station| release_a_bike|

**bike** -> *available_bike* -> **docking_station** -> *release_a_bike* -> **person** -> *use_a_bike*

3.
|object| messages|
------------------
|person| return_a_bike|
|bike|
|docking station| available_space|

**person** -> *return_a_bike* -> **docking_station** -> *available_space?* -> *true/false*

4.
|object| messages|
------------------
|user||
|customer| find_by_surname|

**customer** -> *find_by_surname* -> **user**
