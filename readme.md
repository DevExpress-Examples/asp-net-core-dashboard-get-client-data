<!-- default badges list -->
![](https://img.shields.io/endpoint?url=https://codecentral.devexpress.com/api/v1/VersionRange/363110939/20.2.5%2B)
[![](https://img.shields.io/badge/Open_in_DevExpress_Support_Center-FF7200?style=flat-square&logo=DevExpress&logoColor=white)](https://supportcenter.devexpress.com/ticket/details/T994661)
[![](https://img.shields.io/badge/📖_How_to_use_DevExpress_Examples-e9f6fc?style=flat-square)](https://docs.devexpress.com/GeneralInformation/403183)
[![](https://img.shields.io/badge/💬_Leave_Feedback-feecdd?style=flat-square)](#does-this-example-address-your-development-requirementsobjectives)
<!-- default badges end -->
*Files to look at*:
- [client-data.js](./CS/AspNetCoreDashboard_ClientData/wwwroot/js/client-data.js)
- [_Layout.cshtml](./CS/AspNetCoreDashboard_ClientData/Pages/_Layout.cshtml)
- [Index.cshtml](./CS/AspNetCoreDashboard_ClientData/Pages/Index.cshtml)

# ASP.NET Core Dashboard - How to obtain a dashboard item's client data

The example uses the Dashboard Control's [client-side API](https://docs.devexpress.com/Dashboard/400192/web-dashboard/aspnet-core-dashboard-control/client-side-api-overview) to obtain client data that corresponds to a particular visual element.

The [ViewerApiExtensionOptions.onItemClick](https://docs.devexpress.com/Dashboard/js-DevExpress.Dashboard.ViewerApiExtensionOptions?p=netframework#js_devexpress_dashboard_viewerapiextensionoptions_onitemclick) event is handled to obtain client data and invoke the [dxPopup](https://js.devexpress.com/DevExtreme/ApiReference/UI_Components/dxPopup/) component with the [dxChart](https://js.devexpress.com/DevExtreme/ApiReference/UI_Components/dxChart/).

In the event handler, the `e.getData` method is called to obtain dashboard item's client data. The `e.getAxisPoint` method returns the axis point that corresponds to the clicked card while the [ItemData.getSlice](https://docs.devexpress.com/Dashboard/js-DevExpress.Dashboard.Data.ItemData?p=netframework#js_devexpress_dashboard_data_itemdata_getslice_value_) method returns the slice of client data by this axis point.

The [ItemDataAxis.getPoints](https://docs.devexpress.com/Dashboard/js-DevExpress.Dashboard.Data.ItemDataAxis#js_devexpress_dashboard_data_itemdataaxis_getpoints) method is used to obtain axis points that belong to the "Sparkline" data axis. Corresponding actual/target values are obtained using the [ItemData.getDeltaValue(deltaId)](https://docs.devexpress.com/Dashboard/js-DevExpress.Dashboard.Data.ItemData#js_devexpress_dashboard_data_itemdata_getdeltavalue_deltaid_) method.

When you click a card, `dxChart` displays the detailed chart and shows a variation of actual/target values over time.

## Documentation

- [Client-Side API Overview for ASP.NET Core Dashboard](https://docs.devexpress.com/Dashboard/400192/web-dashboard/aspnet-core-dashboard-control/client-side-api-overview)
- [Obtain Underlying and Displayed Data in Dashboard Control for JavaScript Applications
](https://docs.devexpress.com/Dashboard/403003/web-dashboard/dashboard-control-for-javascript-applications-jquery-knockout-etc/obtain-underlying-and-displayed-data)

## More Examples

- [ASP.NET Core Dashboard - How to obtain a dashboard item's underlying data for a clicked visual element](https://github.com/DevExpress-Examples/asp-net-core-dashboard-get-underlying-data-for-clicked-item)
- [ASP.NET Core Dashboard - How to obtain underlying data for the specified dashboard item](https://github.com/DevExpress-Examples/asp-net-core-dashboard-display-item-underlying-data)
- [ASP.NET Web Forms Dashboard Control - How to obtain a dashboard item's client data](https://github.com/DevExpress-Examples/how-to-obtain-a-dashboard-items-client-data-in-the-aspnet-dashboard-control-t492284)
- [ASP.NET Web Forms Dashboard Control - How to obtain a dashboard item's underlying data for a clicked visual element](https://github.com/DevExpress-Examples/aspxdashboard-how-to-obtain-a-dashboard-items-underlying-data-for-a-clicked-visual-element-t492257)
- [ASP.NET Web Forms Dashboard Control - How to obtain underlying data for the specified dashboard item](https://github.com/DevExpress-Examples/aspxdashboard-how-to-obtain-underlying-data-for-the-specified-dashboard-item-t518504)
<!-- feedback -->
## Does this example address your development requirements/objectives?

[<img src="https://www.devexpress.com/support/examples/i/yes-button.svg"/>](https://www.devexpress.com/support/examples/survey.xml?utm_source=github&utm_campaign=asp-net-core-dashboard-get-client-data&~~~was_helpful=yes) [<img src="https://www.devexpress.com/support/examples/i/no-button.svg"/>](https://www.devexpress.com/support/examples/survey.xml?utm_source=github&utm_campaign=asp-net-core-dashboard-get-client-data&~~~was_helpful=no)

(you will be redirected to DevExpress.com to submit your response)
<!-- feedback end -->
