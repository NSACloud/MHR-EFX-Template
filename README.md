# MHR EFX Template
EFX 010 template for Monster Hunter Rise.

Not all attributes are fully mapped yet. 

If you find out what any of the unknowns do, submit a pull request or an issue and I'll add the changes.

Set the character set to UTF-8 in View > Character Set

Read the template for notes. 

## Installation
Requires **[010 Editor](https://www.sweetscape.com/010editor/)**

Install the template under Templates > View Installed Templates > Add

## Change Log
```
V6 7/1/2022
-----
Reworked template structure to allow for iteration over attributes.
Moved field parameters to be parsed after actions
Changed unkn8 in header to unknFlag
-----
V5 6/25/2022
-----
	Added full sunbreak update support. New structs added. All efx files in sunbreak should work upon release.
	Added path entry to field parameters
	Droppped support for pre sunbreak update efx. Use the pre sunbreak efx template for pre sunbreak efx.
-----
V4 5/29/2022
-----
	Template now works on all efx files in the game (As of pre Sunbreak expansion)
	Added used values for all variables as comments on the template to make mapping their function easier
	Automated data type mapping for unknown variables
	Changed item type to an enum to make porting the template between games easier
	Changed "Parent Options relation" to "Bone Attribute relation", any efx attributes that use bones have a bone attribute relation entry
	Changed unknParameter to expressionParameter
	Moved field parameter values into subheader
	Template forces endian mode to little endian to prevent issues
-----

V3 2/11/2022
-----
	Changed unknEFXValue in subheader to efxParentOptionsRelation
		- Now displays efx entry that the relation entry is associated with
	Changed unkn1 in ParentOptions to isUsingBone
-----

V2 4/24/2021
-----
	Fixed missing float on TypeRibbonFollow. 
	Labeled unknowns for Life, UVSequence, Spawn, TypeMesh - Thank you to thezippotm and Crimson 
-----
```
## Credits

Thank you to:
* **[wwylele](https://github.com/wwylele)** - TDB Dump
* **Crimson** - Labeling Unknowns
* **thezippotm** - Labeling Unknowns