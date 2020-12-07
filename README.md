# Import-Named-Imports

To import variables that are declared, we simply use the original syntax that describes the variable name. In other words, exporting upon declaration does not have an impact on how we import the variables.

import { specialty, isVegetarian } from 'menu';


### QQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQ


1.
Add meetsSpeedRangeRequirements to the import statement at the top of the file.


Hint
import {availableAirplanes, flightRequirements, meetsStaffRequirements, meetsSpeedRangeRequirements} from './airplane';
2.
Define a function displaySpeedRangeStatus().


Hint
function displaySpeedRangeStatus() {
 
}
 
3.
Within the displaySpeedRangeStatus() function, use the forEach method to iterate over each element in the availableAirplanes array.

Again, the forEach() should take a function as a parameter; this function should take element as a parameter.


Hint
function displaySpeedRangeStatus() { 
  availableAirplanes.forEach(function(element){});
}
4.
Within the displaySpeedRangeStatus() function, use console.log() to output the element’s name.


Hint
function displaySpeedRangeStatus() {
  availableAirplanes.forEach(function(element) {
   console.log(element.name);
  });
}
5.
Continuing within the displaySpeedRangeStatus() function, modify the console.log() statement to output a statement like this:

(element name) + 'meets speed range requirements: ' + (true/false)
To do this, we can call the meetsSpeedRangeRequirements method, passing in three parameters element.maxSpeed, element.minSpeed and flightRequirements.requiredSpeedRange.


Hint
function displaySpeedRangeStatus() {
  availableAirplanes.forEach(function(element) {
   console.log(element.name + ' meets speed range requirements: ' + meetsSpeedRangeRequirements(element.maxSpeed, element.minSpeed, flightRequirements.requiredSpeedRange));
  });
}
6.
Call the displaySpeedRangeStatus() function.


Hint
displaySpeedRangeStatus();
