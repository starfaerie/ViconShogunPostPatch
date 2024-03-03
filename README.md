# Vicon ShogunPost Utility Patches
These commands are intended to replace several default System command in ShogunPost which have a bug introduced in ShogunPost 1.10 that throws an error when accessing either a NetApp volume or a filepath that does not yet exist.

These commands all assume that file paths contain backslashes rather than forward slashes, so I've included the utility '_getFile_internal_pathFix.hsl_' with these commands which uses '_strReplace_' to fix input that contains forwardslashes rather than backslashes. This utility command makes these scripts compatible with all other known out of the box System commands in ShogunPost 1.10+ so they can be used as direct substitutes.
| Default ShogunPost Command | Replacement Patched Command |
|:------------:|:----------:|
| getFileTitle | getFileTitle_patched |
| getFileName | getFileName_patched |
| getFileExtension | getFileExtension_patched |
| getFileLocation | getFileLocation_patched |

# Example usage
I've included the example file '_ExampleUsage_' to show a common usecase for these commands where after using the '_getLastFile_' or '_getSavePath_' commands the user wants to use that as an input for one of the default System commands. Instead, these patched commands are substituted. To use these commands just download this project and add it to your Scipts directory, or open it directly from the [Script Editor](https://docs.vicon.com/display/Shogun110/Load+scripts+from+the+HSL+Script+Editor).
