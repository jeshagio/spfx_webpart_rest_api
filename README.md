# SPFX Webpart pulling REST API data.

## Summary

This is spfx Webpart example for pulling and showing information provided by external REST API.

![screenshot](https://github.com/jeshagio/spfx_webpart_rest_api/blob/main/images/webpart-data-external-api.png)

## Used SharePoint Framework Version

![version](https://img.shields.io/badge/version-1.16.1-green.svg)

## Applies to

- [SharePoint Framework](https://aka.ms/spfx)
- [Microsoft 365 tenant](https://docs.microsoft.com/en-us/sharepoint/dev/spfx/set-up-your-developer-tenant)

> Get your own free development tenant by subscribing to [Microsoft 365 developer program](http://aka.ms/o365devprogram)


## Contributors

| Solution    | Author(s)                                               |
| ----------- | ------------------------------------------------------- |
| src | Jorge Ruiz Caro Larrea |

## Version history

| Version | Date             | Comments        |
| ------- | ---------------- | --------------- |
| 1.0     | January 27, 2023 | Initial release |

## Disclaimer

**THIS CODE IS PROVIDED _AS IS_ WITHOUT WARRANTY OF ANY KIND, EITHER EXPRESS OR IMPLIED, INCLUDING ANY IMPLIED WARRANTIES OF FITNESS FOR A PARTICULAR PURPOSE, MERCHANTABILITY, OR NON-INFRINGEMENT.**

---

## Minimal Path to Awesome

- Add a new dir for the solution (with name for example: webpart)
- Ensure that you are at the solution folder
- Clone this repository (https://github.com/jeshagio/spfx_webpart_rest_api.git)
- in the command-line run:
  - **npm install**
- From code editor (recommended Visual Studio Code), open server.json and replace the initialPage parameter with your Sharepoint Online site:
![screenshot](https://github.com/jeshagio/spfx_webpart_rest_api/blob/main/images/webpart-change-sharepoint-url.png)
-  in the command-line run:
  - **gulp serve**
- On the initial page you can add the webpart called "Webpart" and see a list of NBA teams (using the REST API at https://www.balldontlie.io/api/v1/teams)
> If you want to change the url API and show another data just go to src/webparts/webpart/WebpartWebPart.ts, and change the this.context.httpClient.get first parameter, then chek to response.data.forEach((item: any).. , response result will change depending the json returned, and finally check the name of the data you will show: <span class="ms-font-l">${item.full_name}</span> , full_name would change for example by "name"
![screenshot](https://github.com/jeshagio/spfx_webpart_rest_api/blob/main/images/webpart-data-external-api.png)

## References

- [More free APIs for testing at ](https://mixedanalytics.com/blog/list-actually-free-open-no-auth-needed-apis/)

