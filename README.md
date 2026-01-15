# tt-data
Collection of NUSH Timetables in JSON.

## Structure
The directories are in order of `year/sem/level/class/day.json`. For example, the timetable on Monday for class 202 in Semester 1 of 2026 would be in `2026/s1/2/02/mon.json`.
### JSON structure
The JSON file is an array of objects. for each object, there are 3 properties:

`courseCode`: The course code of the lesson, or `null` for free periods(recess/lunch/break), PE and CCE.

`subject`: The subject of the current lesson/free period.
A table of subject names is given below. 

`time`: An array with 2 strings: the start and end times of the lesson, in 24hr time. 

### Notes
For periods where students in the same class are taking different lessons (such as electives or Mother Tongue), the course code is `null`, and there will be an `id` property. 

A list of the different courses is in `year/sem/level/variables.json`.

Breaks that come directly before or after recess/lunch are considered to be part of the recess/lunch.
Free periods that come after the last lesson will not be included.

**Subject Names**

(Only includes subject names that are not the one found in [the POS](https://nush.link/pos))\
(Note that the subject name can be the same as the course code)

Course Code | Subject
 :--------: | :-----:
BL | Bio
CE | CCE
CM | Chem
EC | Econ
EL | English
EN | Eng Lit
GE | Geog
HY | Hist
HU | Hum
MA | Math
PE | PE

## Contributing
If your class isn't here, [create an issue](https://github.com/Spleefies/tt-data/issues/new) with your timetable attached or open a pull request. 