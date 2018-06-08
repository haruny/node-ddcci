# node-ddcci

## Installation

````bash
npm install @hensm/ddcci
````

## Usage

````js
const ddcci = require("ddcci");

for (const monitor of ddcci.getMonitorList()) {
    console.log(`${monitor} current brightness: ${ddcci.getBrightness(monitor)}`);
    ddcci.setBrightness(monitor, 25);
}
````

## Docs

* ### `getMonitorList()`
  Gets a list of the current connected monitors.
  #### Return value
  An array of `String` containing the monitor names.

* ### `getBrightness(monitorName)`
  Queries a monitor's contrast level.
  * #### Parameters
    * **`monitorName`**  
      `String`. Name of monitor for which to query the brightness.
  * #### Return value
    An `integer` between 0-100 representing the current brightness.

* ### `setBrightness(monitorName, level)`
  Sets a monitor's brightness level.
  * #### Parameters
    * **`monitorName`**  
      &emsp;`String`. Name of monitor for which to set the brightness.
    * **`level`**  
      &emsp;`integer`. Between between 0-100 representing the new brightness level.

* ### `getContrast(monitorName)`
  Queries a monitor's contrast level.
  * #### Parameters
    * **`monitorName`**  
      `String`. Name of monitor for which to query the contrast.
  * #### Return value
    An `integer` between 0-100 representing the current contrast.

* ### `setContrast(monitorName, level)`
  Sets a monitor's contrast level.
  * #### Parameters
    * **`monitorName`**  
      &emsp;`String`. Name of monitor for which to set the contrast.
    * **`level`**  
      &emsp;`integer`. Between between 0-100 representing the new contrast level.

* ### `_getVCP(monitorName, vcpCode)`
  Queries a monitor for a VCP code value.
  * #### Parameters
    * **`monitorName`**  
      &emsp;`String`. Name of monitor for which to query the VCP feature.
    * **`vcpCode`**  
      &emsp;`integer`. VCP code to query

* ### `_setVCP(monitorName, vcpCode, value)`
  Sets the value of a VCP code for a monitor.
  * #### Parameters
    * **`monitorName`**  
      &emsp;`String`. Name of monitor for which to set the VCP feature.
    * **`vcpCode`**  
      &emsp;`integer`. VCP code to set.
    * **`value`**  
      &emsp;`integer`. Value of the VCP code.

* ### `_refresh()`
  Refreshes the monitor list.

