# MHR EFX Template
EFX 010 template for Monster Hunter Rise.

Not all attributes are fully mapped yet. 

If you find out what any of the unknowns do, submit a pull request or an issue and I'll add the changes.

Be sure to change the character set to UTF-8 in View > Character Set or text will be garbled.

Read the template for notes. 

## EFX Color Change Script
![image](https://user-images.githubusercontent.com/46909075/213036601-b4a7c37e-c38a-44b3-a565-515ad376d55c.png)


![image](https://user-images.githubusercontent.com/46909075/213037217-9c32443a-156d-4b40-8204-98c98aaa8b95.png)

The **EFX_COLOR_CHANGE.1sc** script allows you to change the color of all entries in an EFX file. To use it, first install it under Scripts > View Install Scripts > Add.

Then with an EFX file open, run the script from the Scripts menu.

There are configurable options if you open the script file. You can enable or disable changing the colors of certain structs and also set the default colors.

The script is not intended to do all of the work. It will not work perfectly in all cases and you may have to manually tweak some things.

## Installation
Requires **[010 Editor](https://www.sweetscape.com/010editor/)**

Install the template under Templates > View Installed Templates > Add

## Change Log
```
V7 1/17/2023
-----
Usability Improvements:
    -   EFX entries can now be parented to a bone easily by entering a bone name in ParentOptions attributes. 
        The template will handle all of the necessary changes to make it work.
Labeled more color attributes
Labeled some unknowns related to collision effects
-----
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
