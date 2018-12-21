## ShowAppMenu

Type
: Function

Sender
: SDL

Purpose
: Request to show the built-in menu view

UI.ShowAppMenu represents a request from an application to open the built-in app-menu which is provided by the native UI.  
This RPC can be sent to the HMI for a projection application that is registered and in the level HMI_FULL with System context being MAIN or MENU. Otherwise it should not be allowed for an app to show the apps menu.

!!! must

  1. Display the built-in menu view previously added via AddSubMenu.
  
!!!

### Request

#### Parameters

|Name|Type|Mandatory|Additional|Description|
|:---|:---|:--------|:---------|:----------|
|menuID|Integer|false||If omitted the HMI opens the apps menu. <br> If set to a sub-menu ID the HMI opens the corresponding sub-menu previously added using AddSubMenu.|


### Response

#### Parameters

This RPC has no additional parameter requirements

### Sequence Diagrams
ShowAppMenu

![ShowAppMenu]()

### Example Request

```json
{
  "id" : 112,
  "jsonrpc" : "2.0",
  "method" : "UI.ShowAppMenu",
  "params" :
  {
    "menuID" : 345
  }
}
```

### Example Response

```json
{
  "id" : 112,
  "jsonrpc" : "2.0",
  "result" :
  {
    "code" : 0,
    "method" : "UI.ShowAppMenu"
  }
}
```
