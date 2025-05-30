# Package Sorting Function

This Python script contains a function designed to classify packages based on their size and weight. The resulting category guides the robotic arm in dispatching each package to the appropriate handling stack within the automation factory, ensuring efficient processing and management.

Function: sort(width, height, length, mass)

Purpose: Classify a package into one of three categories:
- STANDARD: Neither bulky nor heavy
- SPECIAL: Either bulky or heavy, but not both
- REJECTED: Both bulky and heavy

Parameters:
- width (int or float): The width of the package in centimeters.
- height (int or float): The height of the package in centimeters.
- length (int or float): The length of the package in centimeters.
-  mass (int or float): The mass of the package in kilograms.

How It Works:
- Bulky: A package is considered bulky if: Its volume (width * height * length) is ≥ 1,000,000 cm³, or any single dimension (width, height, or length) is ≥ 150 cm.
- Heavy: A package is considered heavy if its mass is ≥ 20 kg.

Based on these conditions, the package is categorized:
- REJECTED if both bulky and heavy.
- SPECIAL if bulky or heavy (but not both).
- STANDARD if neither bulky nor heavy.

Returns a string indicating the category: 'STANDARD', 'SPECIAL', or 'REJECTED'.
