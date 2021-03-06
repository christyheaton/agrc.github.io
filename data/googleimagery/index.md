---
layout: page
status: publish
published: true
title: Google Imagery Information
author:
display_name: Rick Kelson
login: rkelson
email: rkelson@utah.gov
url: ''
author_login: rkelson
author_email: rkelson@utah.gov
wordpress_id: 16519
wordpress_url: http://gis.utah.gov/?page_id=16519
date: '2015-02-09 08:00:09 -0700'
date_gmt: '2015-02-09 15:00:09 -0700'
categories: []
tags:
- agrc
- imagery
- google
- hi res
---
### Background
{: .text-left}

At the beginning of 2015, a coalition of state, regional, and local government agencies purchased a license to Google's high resolution (6 inch pixels) aerial photography. _Read the original [post]({{site.baseurl}}{% post_url 2015-02-02-utah-acquires-high-resolution-aerial-photography-license %}) about the acquisition_. The license will allow Utah's **cities, counties, special districts, state agencies, K12/Higher ed, and tribes** to use this imagery in web and desktop mapping  applications as a streaming web service or, where needed, on premise from downloaded local files. Also included is **use by contractors and formal partners of the immediate licensees**.

### Coordinate System and Datum
{: .text-left}

The native coordinate system for the Google files and services is Web Mercator with a WGS 1984 datum. Many end users in Utah work in coordinate systems with a different datum (NAD 1983 for example). It will be critical for end users that require the highest locational precision to set up their working environment through the use of the appropriate geographic transformation (Esri software users should use NAD_1983_To_WGS_1984_5). The geographic transformation parameter is needed to overcome the locational difference between the WGS84 and NAD83 datum's “realization points” that are about a meter apart. Without the proper geographic transformation, reprojection algorithms will not be able to resolve the last meter of positional accuracy. In order for the imagery to be positioned as accurately as possible when there is a difference between the native projection and datums of the imagery and the client viewing application, a datum conversion must be set (<a href="{{ "/downloads/Transformation.png" | prepend: site.baseurl }}">see example</a>). For ArcMap users, the appropriate datum conversion for Utah is NAD_1983_To_WGS_1984_5. The default (no transformation specified) will likely introduce several feet of horizontal positional error. More information : <a href="http://support.esri.com/en/knowledgebase/techarticles/detail/24159">NAD_1983_To_WGS_1984_5</a>

### Horizontal Positional Accuracy
{: .text-left}

Stated horizontal positional accuracy of the imagery is expected to achieve or exceed one meter (CE90) in most areas without significant vertical relief. Higher precision is expected in urban areas, where existing supplemental ground control was more abundant.

### Discover Server
{: .text-left}

AGRC’s cloud-based server Discover service provides imagery and base maps services in Open Geospatial Consortium (OGC) standard Web Map Tile Service (WMTS) and Web Map Service (WMS) in the Web Mercator WGS84 projection (wkid: 3857). One featured offering from Discover is statewide 6 inch imagery collected and licensed by Google. Due to this licensed content, access to the Discover server is currently only for **Utah’s cities, counties, special districts, state agencies, K12/Higher education, and tribes and contractors and formal partners of the immediate licensees.** To obtain access to the Discover server you need to fill out and understand the **Organizational Usage Agreement** available from the [Google Imagery License]({{"/data/google-imagery-license/" | prepend: site.baseurl }}) page. Once the Organizational Usage Agreement is completed, you will receive information about the services and URL links to access the Discover server. The URLs to access the server will contain a quad-word (ex. `https://discover.agrc.utah.gov/login/path/your-unique-quad-word/`) unique to each user or organization.

In addition to the Google imagery, Discover contains imagery services for NAIP and historical high and low resolution collections. We are actively working on a solution to providing public domain access to Discover server. Read more about the Discover base map services on [the developer base map pages]({{ "/developer/base-maps/" | prepend: site.baseurl }}).

- Instructions on how to [use the Discover services in ArcMap]({{ "/data/sgid-base-map-services-arcmap/" | prepend: site.baseurl }}).

### Adding a WMTS or WMS service to ArcMap
{: .text-left}

Adding a WMTS service to ArcMap is very simple. Go to `Add Data -> GIS Servers -> Add WMTS Server` and paste the WMTS link you have been provided into the `URL:` line then hit OK. Now navigate to the newly added WMTS **'utah imagery - WMTS on discover.agrc.utah.gov'** by going to `Add Data -> GIS Servers`. If you drill down through the service folders you will find the `utah` layer to add <a href="{{ "/downloads/AddWMTS_tree.jpg" | prepend: site.baseurl }}">(see example)</a>. The WMS service can be added by following the instructions above just substitute `GIS Servers -> Add WMS Server`.

### Archive Services
{: .text-left}

In addition to the statewide `utah` Google imagery service layer there are archive layers available, `utah_2012archive` and `utah_2013archive`. As new imagery is collected and added to the <em>utah</em> layer the older replaced imagery is placed into the layer that corresponds to the year the imagery was originally collected. If you are not seeing the <a href="{{ "/downloads/ArchiveServices.png" | prepend: site.baseurl }}"> archive service layers</a> simply go to ArcCatalog or ArcMap's Catalog Viewer and right-click the GIS Server connection created to access the imagery service and select `Refresh`.

### Flight Dates
{: .text-left}

The dates of each flight block can be downloaded from <a href="ftp://ftp.agrc.utah.gov/UtahSGID_Vector/UTM12_NAD83/INDICES/UnpackagedData/Google_UtahServiceDates/_Statewide/">here</a> as a shapefile, viewed <a href="http://arcg.is/1E0wq3b">here</a> in ArcGIS Online, or utilized through our SDE as layer SGID10.INDICES.Google_UtahServiceDates.

### ArcMap User Considerations
{: .text-left}

If you have not yet received quad-word links to the service (ex. `https://discover.agrc.utah.gov/login/path/your-unique-quad-word/`) that do not require a username and password contact <a href="mailto:rkelson@utah.gov"><strong>Rick Kelson</strong></a>.

ArcMap users experiencing problem with the service may need to clear their local cache by going to the service’s `Layer Properties -> Cache` tab and selecting Clear Local Cache Now. Be patient as this could take several minutes.

**ArcMap 10.1 users** should use the WMS service and not the WMTS. The WMTS in ArcMap 10.1 does not render correctly.

### Adding a WMTS service to CAD
{: .text-left}

Take a look at this <a href="ftp://ftp.agrc.utah.gov/Google/MicroStationGoogleWMS_HowTo.pdf">How To document</a>.

### Usage Tracking
{: .text-left}

To access the GCP services individual organizations will be provided URL links for the service unique to their organization. This will allow for tracking usage metrics and performance of the imagery service. Do not distribute the URL links outside of your organization or division.

### Google Logos
{: .text-left}

<a href="ftp://ftp.agrc.utah.gov/Google/google_logos.zip">Download zipfile of Google logos</a><br />
<img src="{{ "/images/ImageryCGoogle_WhiteTransparent.png" | prepend: site.baseurl }}" alt="white transparent" width="132" height="19"> <img src="{{ "/images/ImageryCGoogle_WhiteOnBlack.png" | prepend: site.baseurl }}" alt="white on black" width="132" height="19">

### Requests for On-Premise Use
{: .text-left}

Request can be made to consume the imagery off-line when the provided imagery service does not suffice or if you are not state, regional, local or tribal government, public safety, K-12, or higher education. Please provide the following information for consideration:
  -	Name & organization:
  - Reason for request:
  - Working on behalf of:
  - Project names:
  - Project locations:

### Frequently Asked questions
{: .text-left}

- From time to time it is suggested that you refresh the connection to the imagery services by right-clicking your service connection, in ArcCatalog or ArcMap's Catalog Viewer, and select the `Refresh`  button to see the latest list of available services.
- Since the Google acquisition flight blocks are not done all at once (as opposed to the NAIP product for example), there will certainly be color and positional changes at flight block boundaries. For large area maps, the color-balanced NAIP may be a more aesthetically pleasing cartographic choice.
- A tile index of the .jp2 images that make up the service is available from our SDE as SGID10.INDICES.Google_Tiles or as a download <a  href="ftp://ftp.agrc.utah.gov/UtahSGID_Vector/UTM12_NAD83/INDICES/UnpackagedData/Google_Tiles/_Statewide/">from here</a>.
- For future updates, Utah can certainly pass along requests to Google for additional update areas or for specific collection periods. But there is no provision in the current contract to create any expectation that those requests will be acted upon.
- AGRC has downloaded a statewide master set of the image files for redistribution, as the download process directly from Google incurs transactional costs for cloud server & bandwidth usage.
- AGRC has a feedback reporting form for imagery users around the state to report imagery and service issues so these can be passed along to Google. The feedback form can be found <a href="https://docs.google.com/a/utah.gov/forms/d/1UGU77SPM_HX0r8zblIs05C-H5mLyRja1gRT7Fu4aKZk/viewform?fbzx=-6743712545663240221">here</a>.
