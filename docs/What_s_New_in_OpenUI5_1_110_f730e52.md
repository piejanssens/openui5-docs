<!-- loiof730e521b6aa4c0882021e488f0a026f -->

| loio |
| -----|
| f730e521b6aa4c0882021e488f0a026f |

<div id="loio">

view on: [demo kit nightly build](https://sdk.openui5.org/nightly/#/topic/f730e521b6aa4c0882021e488f0a026f) | [demo kit latest release](https://sdk.openui5.org/topic/f730e521b6aa4c0882021e488f0a026f)</div>

<link rel="stylesheet" type="text/css" href="css/sap-icons.css"/>

## What's New in OpenUI5 1.110

With this release OpenUI5 is upgraded from version 1.109 to 1.110.

***

<a name="loiof730e521b6aa4c0882021e488f0a026f__section_yxw_pxt_zcb"/>

### New Features


<table>
<tr>
<td valign="top">

**Copy-to-Clipboard Feature for Tables**

Users can copy selected table content to the clipboard and use it anywhere inside or outside an app. To achieve this, we have introduced the new `sap.m.plugins.CopyProvider` plugin. To extract the cell data from the table, we have created the `extractData` property. This new feature is available for grid and responsive tables. For more information, see the [API Reference](https://sdk.openui5.org/api/sap.m.plugins.CopyProvider).



</td>
</tr>
<tr>
<td valign="top">

**`sap.m.p13n.Engine`**

We have provided a new entity that allows custom control developers and application developers to make use of available personalization settings for their controls, for example, for sorting, grouping, and managing variants, and handling personalization states.For more information, see the [API Reference](https://sdk.openui5.org/api/sap.m.p13n.Engine) and the [Sample](https://sdk.openui5.org/entity/sap.m.p13n.Engine/sample/sap.m.sample.p13n.Engine).



</td>
</tr>
</table>

***

<a name="loiof730e521b6aa4c0882021e488f0a026f__section_bkm_s15_zcb"/>

### New Controls


<table>
<tr>
<td valign="top">

**`sap.m.table.ColumnMenu`**

We have introduced a new control that allows users to do the following in grid and responsive tables:

-   Quick sorting

-   Quick filtering

-   Quick grouping

-   Quick selection of columns

-   Quick totaling


These features are available in a menu that users can choose in the column headers of the tables. Applications can define their own application-specific quick actions. For more information, see the  [API Reference](https://sdk.openui5.org/api/sap.m.table.columnmenu)  and the [Sample](https://sdk.openui5.org/entity/sap.ui.comp.smarttable.SmartTable/sample/sap.ui.comp.sample.smarttable). 



</td>
</tr>
</table>

***

<a name="loiof730e521b6aa4c0882021e488f0a026f__section_qwl_pb5_zcb"/>

### Improved Features


<table>
<tr>
<td valign="top">

**Header Bar in Key User Adaptation**

The header bar in key user adaptation has been redesigned.

-   The *Save & Exit* button has been replaced by two separate buttons for *Save* \(:floppy_disk:\) and *Exit* \(:x:\).

-   For each action, an icon is now displayed.

-   Actions that are available in some environments only, like *Translate*, *Manage App Variants*, and *Save As*, have been moved to a *More Actions* menu that key users access by clicking on a new hamburger icon \(<span class="SAP-icons"></span>\).

    When the *More Actions* menu has no entries, like in the demo apps in the SAPUI5 demo kit, the hamburger icon is hidden.


The following screenshot shows an example:

 ![](images/loio00fdcc7e160c4395a3b98824accc64a4_LowRes.png) 



</td>
</tr>
<tr>
<td valign="top">

**OpenUI5 Formatters**

The new version of OpenUI5 introduces the following formatting features:

-   You can now use the `sap-timezone` URL parameter for testing an application in a different time zone by specifying an IANA time zone, such as "America/New\_York". We do not recommend using this parameter in a productive environment. For more information, see [Configuration Options and URL Parameters](Configuration_Options_and_URL_Parameters_91f2d03.md).
-   We have restricted the use of fallback patterns without delimiters in `DateFormat`. Successful parsing now requires that the length matches, as only then year, month, and day values can reliably be attributed.
-   We have updated the OpenUI5 locale data to Version 41 of the Unicode Common Locale Data Repository \(CLDR\). With this upgrade, unit keys have changed incompatibly in the CLDR. A legacy unit mapping ensures that previous unit keys are still supported when formatting. Parsing of user input will provide the current unit keys. For more information, see [Legacy Unit Mapping](Unit_Formatting_8e618a8.md#loio8e618a8d93cb4f92adc911b96047eb8d__section_LUM).



</td>
</tr>
<tr>
<td valign="top">

**OpenUI5 OData V4 Model**

The new version of the OpenUI5 OData V4 model introduces the following features:

-   Requesting `$count` and using `sap.ui.model.odata.v4.ODataListBinding#getDownloadUrl` now work with the experimental hierarchy feature introduced with OpenUI5 1.105. For more information, see the API Reference for [`getDownloadUrl`](https://sdk.openui5.org/api/sap.ui.model.odata.v4.ODataListBinding/methods/getDownloadUrl) and the `hierarchyQualifier` in [`setAggregation`](https://sdk.openui5.org/api/sap.ui.model.odata.v4.ODataListBinding/methods/setAggregation), and[Binding Collection Inline Count](Binding_Collection_Inline_Count_77d2310.md).
-   The `synchronizationMode` model parameter is now optional and deprecated.
-   User input into inactive rows is now regarded as a pending change by `sap.ui.model.odata.v4.Context#hasPendingChanges`; it can be reset using `sap.ui.model.odata.v4.Context#resetChanges`. You can prevent the activation of inactive rows after user input since OpenUI5 1.109 using `sap.ui.base.Event#preventDefault` in the handler of the `createActivate` event.For more information, see the API Reference for [`hasPendingChanges`](https://sdk.openui5.org/api/sap.ui.model.odata.v4.Context/methods/hasPendingChanges), [`resetChanges`](https://sdk.openui5.org/api/sap.ui.model.odata.v4.Context/methods/resetChanges), and [`preventDefault`](https://sdk.openui5.org/api/sap.ui.base.Event/methods/preventDefault).
-   The `sap.ui.model.odata.v4.ODataModel` now supports the `propertyChange` event.For more information, see the [API Reference](https://sdk.openui5.org/api/sap.ui.model.odata.v4.ODataModel/events/propertyChange).



</td>
</tr>
</table>

***

<a name="loiof730e521b6aa4c0882021e488f0a026f__section_rqn_wd5_zcb"/>

### Improved Controls


<table>
<tr>
<td valign="top">

**`sap.m.Carousel`**

Using the new `backgroundDesign` property, you can now set the carousel’s background color as `Translucent` \(Default\), `Solid`, or `Transparent`.For more information, see the [API Reference](https://sdk.openui5.org/api/sap.m.Carousel) and the [Sample](https://sdk.openui5.org/entity/sap.m.Carousel/sample/sap.m.sample.CarouselWithDisplayOptions).



</td>
</tr>
<tr>
<td valign="top">

**`sap.m.ComboBox`**

We have updated the behavior of the `loadItems` API. Now, when the picker is open and no items are loaded - the *No data* label is loaded in the list. For more information, see the [Sample](https://sdk.openui5.org/entity/sap.m.ComboBox/sample/sap.m.sample.ComboBoxLazyLoading).



</td>
</tr>
<tr>
<td valign="top">

**`sap.m.Dialog`**

We have added a new `footer` aggregation of type `sap.m.Toolbar` to the control. You can now use this horizontal container to display controls that fit different custom scenarios, for example, a button that shows a message popover.For more information, see the [API Reference](https://sdk.openui5.org/api/sap.m.Dialog) and the [Sample](https://sdk.openui5.org/entity/sap.m.Dialog/sample/sap.m.sample.DialogWithMessagePopover).



</td>
</tr>
<tr>
<td valign="top">

**`sap.m.IllustratedMessage`**

The `IllustratedMessage`'s sample of the default set of illustrations is now split into three different samples depending on their visual style: classic, illustrative, and simple.

For more information, see the [Samples](https://sdk.openui5.org/entity/sap.m.IllustratedMessage).



</td>
</tr>
<tr>
<td valign="top">

**`sap.m.ObjectStatus`**

We have implemented a new property to give application developers the ability to override the default state announcement. Now the `group` role isn't placed on inactive control instances and a proper `roledescription` is set for active control instances.

 For more information, see the [API Reference](https://sdk.openui5.org/api/sap.m.ObjectStatus). 



</td>
</tr>
<tr>
<td valign="top">

**`sap.m.PlanningCalendar, sap.m.SinglePlanningCalendar`**, and **`sap.ui.core.format.DateFormat`**

We have adapted our Date and Time controls to support the calendar week based on the `sap.ui.core.format.DateFormat` options.

 For more information, see the [API Reference](https://sdk.openui5.org/api/sap.ui.core.format.DateFormat). 



</td>
</tr>
<tr>
<td valign="top">

**`sap.m.SelectDialog` and `sap.m.TableSelectDialog`**

You can now control the placeholder text in the inner search field using the new `searchPlaceholder` property. If not set, the word `Search` in the current local language or in English will be used as a placeholder.

For more information, see the [API Reference](https://sdk.openui5.org/api/sap.m.SelectDialog) and the [Sample](https://sdk.openui5.org/entity/sap.m.SelectDialog/sample/sap.m.sample.SelectDialog).



</td>
</tr>
<tr>
<td valign="top">

**`sap.ui.core.ScrollEnablement`**

We have added a new option to the `scrollToElement` API method of the `sap.ui.core.ScrollEnablement` class. If the new `bSkipElementsInScrollport` parameter is set to `true`, scrolling will happen only if necessary. For more information, see the [API Reference](https://sdk.openui5.org/api/sap.ui.core.delegate.ScrollEnablemen/methods/scrollToElement).



</td>
</tr>
<tr>
<td valign="top">

**`sap.ui.integration.widgets.Card`**

-   List and Object cards can now display \(default\) icons for object attributes of states `Error`, `Warning`, `Success` or `Information`. The icons are shown if the new `showStateIcon` property is set to `true`. For more information, see the [Attributes](https://sdk.openui5.org/test-resources/sap/ui/integration/demokit/cardExplorer/webapp/index.html#/explore/list/attributes) and the [Form Inputs](https://sdk.openui5.org/test-resources/sap/ui/integration/demokit/cardExplorer/webapp/index.html#/explore/object/form) examples in the Card Explorer.

-   We have improved the loading of the libraries that are specified in the `dependencies` attribute of the `sap.ui5` namespace. This option allows you to use other libraries in the card. For more information, see the [Card Manifest](https://sdk.openui5.org/test-resources/sap/ui/integration/demokit/cardExplorer/webapp/index.html#/learn/cardManifest) section and the [Shared Extension](https://sdk.openui5.org/test-resources/sap/ui/integration/demokit/cardExplorer/webapp/index.html#/explore/extension/sharedExtension) example in the Card Explorer.

-   As a card developer, you can now dynamically hide the filters in the card using the new `visible` property. For more information, see the [Multiple Filters](https://sdk.openui5.org/test-resources/sap/ui/integration/demokit/cardExplorer/webapp/index.html#/explore/searchFilter/multipleFilters) example in the Card Explorer.




</td>
</tr>
</table>

***

<a name="loiof730e521b6aa4c0882021e488f0a026f__section_cps_cg5_zcb"/>

### Deprecations


<table>
<tr>
<td valign="top">

There are currently no major deprecations. For a complete list of all deprecations, see [Deprecated APIs](https://sdk.openui5.org/api/deprecated). 



</td>
</tr>
</table>

***

<a name="loiof730e521b6aa4c0882021e488f0a026f__section_r5v_3h5_zcb"/>

### Demo Kit Improvements


<table>
<tr>
<td valign="top">

**Improved main theme selection**

We have added the latest high contrast themes to the main theme selector in the Demo Kit.![](images/loiob76a17bb50f04301b6b21dd28ee048c5_Source1.png) 



</td>
</tr>
</table>

