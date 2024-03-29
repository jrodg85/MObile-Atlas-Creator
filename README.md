<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">
<html>
<head>
<meta http-equiv="Content-Type" content="text/html; charset=UTF-8">
<title>Mobile Atlas Creator - Readme</title>
<style type="text/css">
body {
	margin-left: 10px;
	font-family: Helvetica, Arial, sans-serif;
}

h1,h2,h3,h4 {
	color: #0000CC;
	font-style: italic;
}

h1 {
	border-bottom: solid thin black;
}

h2 {
	margin-left: 20px;
}

h3 {
	margin-left: 50px;
}

h4 {
	margin-left: 80px;
}

pre {
	margin-left: 140px;
}

p,ul,ol {
	font-size: 110%;
	margin-left: 100px;
}
</style>
</head>
<body>
	<h1>Mobile Atlas Creator - Read-me</h1>
	<p>Welcome to Mobile Atlas Creator read-me file for end users.</p>
	<p>Before January 2010 this project was known as "TrekBuddy Atlas
		Creator".</p>
	<p>
		Mobile Atlas Creator is an open source project hosted on
		SourceForge.net: <br> <a href="http://mobac.sf.net">http://mobac.sf.net</a>
	</p>
	<h2>Table of contents</h2>
	<ul style="margin-left: 50px;">
		<li><a href="#License">License</a></li>
		<li><a href="#Description">Description</a></li>
		<li><a href="#Requirements">Requirements</a>
			<ul style="margin-left: 10px;">
				<li><a href="#JAI">Java Advanced Imaging" (JAI)</a></li>
			</ul></li>
		<li><a href="#Installation">Installation</a></li>
		<li><a href="#Start">Application start</a></li>
		<li><a href="#AtlasFormats">The different atlas formats</a>
			<ul style="margin-left: 10px;">
				<li><a href="#AFTrackOSZ">AFTrack (OSZ)</a></li>
				<li><a href="#AlpineQuestMap">AlpineQuestMap (AQM)</a></li>
				<li><a href="#AndNav">AndNav</a></li>
				<li><a href="#BigPlanet">Big Planet Tracks</a></li>
				<!-- CacheBox  -->
				<li><a href="#CacheWolf">CacheWolf</a></li>
				<li><a href="#GarminCustom">Garmin Custom maps</a></li>
				<li><a href="#Glopus">Glopus</a></li>
				<li><a href="#GMF">Glopus Map File / AFTrack (GMF)</a></li>
				<li><a href="#KMZ">Google Earth Overlay (KMZ)</a></li>
				<!-- GPS Sports Tracker -->
				<li><a href="#Magellan">Magellan RMP</a></li>
				<li><a href="#MAPLORER">MAPLORER</a></li>
				<li><a href="#Maverick">Maverick</a></li>
				<li><a href="#MGMaps">MGMaps</a></li>
				<li><a href="#MTE">Mobile Trail Explorer (MTE)</a></li>
				<li><a href="#NaviComputer">NaviComputer</a></li>
				<li><a href="#nfComPass">nfComPass</a></li>
				<li><a href="#OruxMaps">OruxMaps</a></li>
				<li><a href="#OSMAND">OSMAND</a></li>
				<li><a href="#Osmdroid">Osmdroid</a></li>
				<li><a href="#OSMTracker">OSMTracker</a></li>
				<li><a href="#Ozi">OziExplorer / large PNG image</a></li>
				<li><a href="#PathAway">PathAway</a></li>
				<li><a href="#RMaps">RMaps</a></li>
				<li><a href="#SportsTracker">[Nokia] Sports Tracker</a></li>
				<li><a href="#TomTomRaster">TomTom Raster</a></li>
				<li><a href="#TTQV">Touratech QV</a></li>
				<li><a href="#TrekBuddy">TrekBuddy</a></li>
				<li><a href="#TwoNav">TwoNav (RMAP)</a></li>
				<li><a href="#Viewranger">Viewranger</a></li>
				<!-- UBlox -->
			</ul></li>
		<li><a href="#Enhancement">Enhancement requests</a></li>
		<li><a href="#Bugs">Problems, Bugs &amp; Errors</a></li>
		<li><a href="#Limitations">Known problems and limitations</a></li>
		<li><a href="#AdvancedUsers">Details for advanced users</a>
			<ul style="margin-left: 10px;">
				<li><a href="#DirectoryConfig">Specifying directory
						configuration</a></li>
				<li><a href="#TileStoreDir">Moving the tile store directory</a>
				</li>
				<li><a href="#ExternalTools">Starting external tools from
						within MOBAC</a></li>
			</ul>
		<li><a href="#CustomMapSource">Custom map sources</a>
			<ul style="margin-left: 10px;">
				<li><a href="#SimpleCustomMapSource">Simple custom map
						sources</a></li>
				<li><a href="#CustomWMSMapSource">Custom WMS map sources</a></li>
				<li><a href="#CustomMultiLayerMapSource">Custom multi-layer
						map sources</a></li>
				<li><a href="#CloudMadeMapSource">Custom CloudMade map
						sources</a></li>
				<li><a href="#BeanShellMapSource">Custom BeanShell map
						sources</a></li>
				<li><a href="#CustomMapPack">Custom MapPack</a></li>
				<li><a href="#Mapsforge">MOBAC integrated rendering of
						tiles based on OpenStreetmap (mapsforge) vector data</a></li>
				<li><a href="#FileBased">Custom atlas as map source /
						locally generated tiles</a></li>
			</ul></li>
	</ul>
	<hr>

	<h2>
		<a name="License">License</a>
	</h2>
	<p>
		Mobile Atlas Creator is under GNU General Public License Version 2
		(GPL). For details on the GPL see the license file <a href="gpl.txt">gpl.txt</a>.<br>
		The source code is available on the <a
			href="http://sourceforge.net/projects/mobac/files/">SourceForge.net</a>
		for download and in the <a href="http://sourceforge.net/p/mobac/code/">project's
			source code Subversion repository</a>.
	</p>

	<h2>
		<a name="Description">Description</a>
	</h2>
	<p>
		Mobile Atlas Creator creates atlases for several applications. For
		example <a href="http://www.trekbuddy.net">TrekBuddy</a> and <a
			href="http://code.google.com/p/mobile-trail-explorer/">Mobile
			Trail Explorer (MTE)</a>, the Android applications <a
			href="http://www.andnav.org/">AndNav</a>, <a
			href="http://www.codesector.com/maverick.php">Maverick</a>, <a
			href="http://code.google.com/p/big-planet-tracks/">Big Planet
			Tracks</a>, <a
			href="http://robertdeveloper.blogspot.com/search/label/rmaps.release">RMaps</a>,
		<a href="http://www.oruxmaps.com/">OruxMaps</a>, the Pocket PC
		application <a href="http://www.glopus.de/">Glopus</a> and the
		commercial Windows application <a href="http://www.oziexplorer.com/">OziExplorer</a>.
		The map image created for OziExplorer can also be used with any PNG
		capable image viewer (map image in one large PNG file).
	</p>

	<h2>
		<a name="Requirements">Requirements</a>
	</h2>
	<p>This application requires that a Java SE Runtime Environment 7 or higher is installed on the	computer.</p>
	<p>If you have the choice between different Java Runtimes you
		should prefer the Java Runtime provided by Sun/Oracle. Especially the
		OpenJDK has some bugs regarding MOBAC and tends to crash on certain
		situations.</p>
	<h3>
		<a name="JAI">Java Advanced Imaging (optional)</a>
	</h3>
	<p>
		For reducing the color depth of downloaded tiles the library files (
		<tt>jai_core.jar</tt>
		and
		<tt>jai_codec.jar</tt>
		) of the "Java Advanced Imaging" (JAI) have to be present on the
		system respectively in the same directory as Mobile_Atlas_Creator.jar.
		Ready to use binary builds of the Java Advanced Imaging library can be
		obtained at <a
			href="http://download.java.net/media/jai/builds/release/1_1_3/jai-1_1_3-lib.zip">http://download.java.net/media/jai/builds/release/1_1_3/jai-1_1_3-lib.zip</a>
	</p>

	<h2>
		<a name="Installation">Installation</a>
	</h2>
	<p>
		Copy or move the unzipped files to a folder where you would like to
		have Mobile Atlas Creator installed. On computers running Windows
		please make sure <b>not to install MOBAC into <tt>Program
				Files</tt> sub-directory!
		</b>
	</p>

	<h2>
		<a name="Start">Application start</a>
	</h2>
	<h3>Windows</h3>
	<p>
		The application is started by executing the
		<tt>Mobile Atlas Creator.exe</tt>
		. During the first application start all necessary files and folders
		are automatically created by the application.
	</p>
	<h3>Linux and OSX</h3>
	<p>
		You can start MOBAC by executing the start-up script
		<tt>start.sh</tt>
		. Before starting MOBAC the first time it may be necessary to set the
		executable bit for
		<tt>start.sh</tt>
		e.g. by executing the following command:
	</p>
	<pre>chmod u+x start.sh</pre>
	<p>During the first application start all necessary files and
		folders are automatically created by the application.</p>
	<hr>
	<!-- *************************************************************************** -->
	<h2>
		<a name="AtlasFormats">The different atlas formats</a>
	</h2>
	<!-- *************************************************************************** -->
	<h3>
		<a name="AFTrackOSZ">AFTrack OSZ</a>
	</h3>
	<p>
		For creating atlases compatible with AFTrack (Symbian S60) you have to
		select <b>AFTrack (OSZ)</b> as format in atlas format selection dialog
		that appears when starting a new atlas (menu <b>Atlas</b> entry <b>New
			Atlas</b>).
	</p>
	<p>
		OSZ is a ZIP-archive. Within this zip archive a (large) number of
		tiles with the calibrated folder structure (coordinates) are stored.
		OSZ only works if each tile has got a resolution of 256x256 Pixels. So
		be sure to uncheck <b>Recreate/adjust map tiles (CPU intensive)</b>.
	</p>
	<p>The output format is one file for each layer in the
		corresponding folder.</p>
	<h4>
		<a name="AFTrackOSZRestriction">Restrictions</a>
	</h4>
	<p>Depending on the device free memory the file maybe not work. So
		more then 80000 tiles should not be used.</p>
	<!-- *************************************************************************** -->
	<h3>
		<a name="AlpineQuestMap">AlpineQuestMap (AQM)</a>
	</h3>
	<p>Sorry no further details are available for this atlas format.</p>
	<!-- *************************************************************************** -->
	<h3>
		<a name="AndNav">Creating and using atlases with AndNav</a>
	</h3>
	<p>
		For creating atlases compatible with AndNav you have to select <b>AndNav
			atlas format</b> as format in atlas format selection dialog that appears
		when starting a new atlas (menu <b>Atlas</b> entry <b>New Atlas</b>).<br>
		As atlases for AndNav do not support all features provided by Mobile
		Atlas Creator the following settings are ignored when creating atlases
		for AndNav:
	</p>
	<ul>
		<li>Change height or width of the map tiles</li>
		<li>Name of all layers and maps</li>
		<li>Structure of the atlas (which maps belongs to which layer)</li>
	</ul>
	<!-- *************************************************************************** -->
	<h3>
		<a name="BigPlanet">Creating and using atlases with Big Planet
			Tracks</a>
	</h3>
	<p>
		For creating offline atlases compatible with <a
			href="http://code.google.com/p/big-planet-tracks/">Big Planet
			Tracks</a> (Android application) you have to select <b>Big Planet
			Tracks SQLite</b> as format in atlas format selection dialog that appears
		when starting a new atlas (menu <b>Atlas</b> entry <b>New Atlas</b>).<br>
		The atlas format BigPlanet SQLite does not support all features
		provided by Mobile Atlas Creator the following settings can not be
		used or are ignored when creating atlases using this output format:
	</p>
	<ul>
		<li>Recreate/adjust map tiles with custom tile size (height and
		<li>Name of all layers and maps</li>
		<li>Structure of the atlas (which maps belongs to which layer)</li>
		<li>Atlases created after another are merged into one Database
			named <tt>[Atlasname] atlas.sqlitedb</tt> which is located in the
			atlas output directory.
		</li>
	</ul>
	<!-- *************************************************************************** -->
	<h3>
		<a name="CacheWolf">Creating atlases for CacheWolf</a>
	</h3>
	<p>
		For creating atlases compatible with <a href="http://www.cachewolf.de">CacheWolf</a>
		you have to select <b>CacheWolf WFL</b> as format in atlas format
		selection dialog that appears when starting a new atlas (menu <b>Atlas</b>
		entry <b>New Atlas</b>).
	</p>
	<h4>Custom tile processing settings enabled</h4>
	<p>Maps that have custom tile processing options set are saved as
		tiled images with one WFL calibration file for each tile. All
		processing options such as image format and tile size can be used.</p>
	<h4>Custom tile processing settings disabled</h4>
	<p>
		In this mode automatic tiling is disabled and the same <a
			href="#OziRestriction">restrictions</a> and the <a href="#OziWarning">warning</a>
		as for the OziExplorer output format apply.
	</p>
	<p>
		The output format of an "atlas" for CacheWolf is one subdirectory per
		layer and within this subdirectory one
		<tt>PNG</tt>
		image and one
		<tt>WFL</tt>
		file per defined map.
	</p>
	<!-- *************************************************************************** -->
	<h3>
		<a name="GarminCustom">Creating Garmin Custom maps</a>
	</h3>
	<p>
		For creating atlases of Creating Garmin Custom maps you have to select
		<b>Garmin Custom Map (KMZ)</b> as format in atlas format selection
		dialog that appears when starting a new atlas (menu <b>Atlas</b> entry
		<b>New Atlas</b>).<br> Details about the Garmin Custom Map format
		can be found in the <a
			href="https://forums.garmin.com/forumdisplay.php?f=205">Garmin
			Forums</a>
	</p>
	<p>Using this atlas output format the following features are
		ignored when creating atlases:</p>
	<ul>
		<li>Recreate/adjust map tiles (custom tile size and image format)</li>
	</ul>
	<p>
		The output format of an "atlas" for Garmin Custom maps is one
		<tt>KMZ</tt>
		file per layer containing all maps (max 100) as seperate
		<tt>JPG</tt>
		image files. The JPEG compression rate can be specified for each
		map/image using image format selector in the custom tile processing
		section. The Garmin Custom Map format defines a maximum image size of
		1024x1024 pixels. If a map is larger it will be automatically scaled
		down to fit into this size. You can prevent scaling when setting the
		max map size in the settings dialog to 1024.
	</p>
	<!-- *************************************************************************** -->
	<h3>
		<a name="Glopus">Creating atlases for Glopus</a>
	</h3>
	<p>
		For creating atlases compatible with Glopus you have to select <b>Glopus
			(PNG &amp; KAL)</b> or <b> Glopus Map File (GMF)</b> as format in atlas
		format selection dialog that appears when starting a new atlas (menu <b>Atlas</b>
		entry <b>New Atlas</b>).
	</p>
	<h4>Glopus (PNG &amp; KAL)</h4>
	<p>
		Using this atlas output format the same <a href="#OziRestriction">restrictions</a>
		and the <a href="#OziWarning">warning</a> as for the OziExplorer
		output format apply.
	</p>
	<p>
		The output format of an "atlas" for Glopus is one subdirectory per
		layer and within this subdirectory one
		<tt>PNG</tt>
		image and one
		<tt>KAL</tt>
		file per defined map.
	</p>
	<h4>Glopus Map File (GMF)</h4>
	<p>
		Within this file a (large) number of tiles with its calibrated
		coordinates are stored. Glopus works best if each tile has a
		resolution of 1024x1024 pixels. So check <b>Recreate/adjust map
			tiles (CPU intensive)</b>. Width and height should be set to <b>1024</b>.
	</p>
	<p>The output format is one file for each layer in the
		corresponding folder.</p>
	<!-- *************************************************************************** -->
	<h3>
		<a name="GMF">Glopus Map File (GMF) / AFTrack</a>
	</h3>
	<p>
		For creating atlases compatible with AFTrack (Symbian S60) you have to
		select <b>Glopus Map File (GMF)</b> as format in atlas format
		selection dialog that appears when starting a new atlas (menu <b>Atlas</b>
		entry <b>New Atlas</b>).
	</p>

	<p>
		Within this file a (large) number of tiles with its calibrated
		coordinates are stored. AFTrack works best if each tile has got a
		resolution of 256x256 Pixels. So uncheck <b>Recreate/adjust map
			tiles (CPU intensive)</b>.
	</p>
	<p>The output format is one file for each layer in the
		corresponding folder.</p>
	<h4>
		<a name="AFTrackRestriction">Restrictions</a>
	</h4>
	<p>AFTrack can handle a maximum of 4096 tiles - so be sure not to
		select more.</p>
	<!-- *************************************************************************** -->
	<h3>
		<a name="KMZ">Google Earth Overlay (KMZ)</a>
	</h3>
	<p>
		For creating Google Earth Overlays you have to select <b>Google
			Earth Overlay (KMZ)</b> as format in atlas format selection dialog that
		appears when starting a new atlas (menu <b>Atlas</b> entry <b>New
			Atlas</b>).
	</p>
	<p>Using this atlas output format the following features are
		ignored when creating atlases:</p>
	<ul>
		<li>Recreate/adjust map tiles (custom tile size and image format)</li>
	</ul>
	<h4>Warning</h4>
	<p>
		The Google Earth Overlay atlas format uses JPG images. The image size
		depends on the selected maximum map size (see settings dialog). The
		theoretical maximum map size for this atlas format is 25000. However
		it is <b>strongly recommended not to set the maximum map size
			higher than 10000</b> (this will result in a image with uncompressed size
		about 286 MB).
	</p>
	<!-- *************************************************************************** -->
	<h3>
		<a name="Magellan">Creating Magellan RMP atlases</a>
	</h3>
	<p>
		For creating atlases of Creating Garmin Custom Maps you have to select
		<b>Magellan (RMP)</b> as format in atlas format selection dialog that
		appears when starting a new atlas (menu <b>Atlas</b> entry <b>New
			Atlas</b>).
	</p>
	<p>Using this atlas output format the following features are
		ignored when creating atlases:</p>
	<ul>
		<li>Recreate/adjust map tiles (custom tile size and image format)</li>
	</ul>
	<p>Additionally some other limitations may apply, based on which
		device and firmware version you are using. Mobile Atlas Creator does
		not chek those limitations - therefore it may work or not if you are
		using:</p>
	<ul>
		<li>An atlas with more than 5 maps.</li>
		<li>Maps with a zoom level higher than 15.</li>
	</ul>
	<p>
		The output format of an "atlas" for Magellan is one
		<tt>RMP</tt>
		file in the atlas directory. You can directly load this file in
		Magellan VantagePoint or transfer it onto your device.
	</p>
	<!-- *************************************************************************** -->
	<h3>
		<a name="MAPLORER">Creating atlases for MAPLORER</a>
	</h3>
	<p>
		For creating atlases compatible with <a href="http://maplorer.com">MAPLORER</a>
		you have to select the <b>Maplorer atlas format</b> as format in atlas
		format selection dialog that appears when starting a new atlas (menu <b>Atlas</b>
		entry <b>New Atlas</b>). You have to choose <b>JPG image format</b>
		under <b>Layer settings/tile format</b> (PNG is not supported by
		Maplorer).
	</p>

	<p>
		There are no specific limits on tile sizes and/or numbers; good
		results for hiking/biking can be obtained using zoom level 15, custom
		tile size of 1024x1024 (check <b>Recreate/adjust map tiles (CPU
			intensive)</b> under <b>Layer settings</b>. For good performance, avoid
		using too big or too many tiles (the maximum number of columns in
		Maplorer is currently 26 ('A' to 'Z'), but it is preferable to use
		less).
	</p>

	<p>
		After defining the maps and layers (select region and click <b>Add
			selection</b> under <b>Atlas Content)</b> for the atlas, click the button
		Create Atlas. Once atlas download and creation has completed, all
		necessary files belonging to the atlas can be found in the directory
		<tt>atlases\[atlas name]_[current date and time]</tt>
		.
	</p>

	<p>
		To install the atlas on your device, simply connect it to your PC and
		copy the content of the respective atlas subdirectory (i.e. all .jpg
		and .pos files generated) to the Maplorer directory (the one which
		contains maplorer.exe) on your device. Starting Maplorer on the device
		will automatically read all tiles and create the index map. Detailed
		instructions on making maps for Maplorer can be found at <a
			href="http://maplorer.com">http://maplorer.com</a>
	</p>
	<!-- *************************************************************************** -->
	<h3>
		<a name="Maverick">Creating and using atlases with Maverick</a>
	</h3>
	<p>
		For creating atlases compatible with Maverick you have to select <b>Maverick
			atlas format</b> as format in atlas format selection dialog that appears
		when starting a new atlas (menu <b>Atlas</b> entry <b>New Atlas</b>).<br>
		As atlases for Maverick do not support all features provided by Mobile
		Atlas Creator the following settings are ignored when creating atlases
		for AndNav:
	</p>
	<ul>
		<li>Recreate/adjust map tiles (custom tile size and image format)</li>
		<li>Name of all layers and maps</li>
		<li>Structure of the atlas (which maps belongs to which layer)</li>
	</ul>
	<p>
		For further information how to use offline atlases with Maverick
		please see <a href="http://help.codesector.com/MapsCache">Maverick
			Online Help on Setting up offline maps</a>.
	</p>
	<!-- *************************************************************************** -->
	<h3>
		<a name="MGMaps">Creating and using atlases with MGMaps</a>
	</h3>
	<p>
		For creating atlases compatible with MGMaps you have to select <b>MGMaps</b>
		as format in atlas format selection dialog that appears when starting
		a new atlas (menu <b>Atlas</b> entry <b>New Atlas</b>). Select a name
		for the maps, this is important as you will use it to view the maps in
		MGMaps.
	</p>
	<h4>How to copy the maps to your device</h4>
	<ol>
		<li>Create a folder named <tt>MGMapsCache</tt> in the root of you
			device or memorycard
		</li>
		<li>Copy the created folders into this MGMapsCache folder so the
			directory structure looks like:</li>
	</ol>
	<pre>
MGMapsCache
MGMapsCache\cache.conf
MGMapsCache\macos_10
MGMapsCache\macos_11
MGMapsCache\macos_12
MGMapsCache\macos_10\59_53.mgm
MGMapsCache\macos_11\150_106.mgm
MGMapsCache\macos_11\150_107.mgm
MGMapsCache\macos_11\151_106.mgm
MGMapsCache\macos_11\151_107.mgm
MGMapsCache\macos_12\365_213.mgm
MGMapsCache\macos_12\365_214.mgm
MGMapsCache\macos_12\366_213.mgm
MGMapsCache\macos_12\366_214.mgm
	</pre>
	<h4>How to set up MGMaps to use the maps</h4>
	<ol>
		<li>Select Settings/Map/Stored Maps, Click on the two boxes
			labelled Stored Maps and Offline Mode. The first box enables the use
			of stored map mode. The second box prohibits the use of the mobile
			phones Internet connect to download live maps. You can leave this
			unchecked if you want. stored maps folder: now tell MGMaps where you
			have stored the map tile files. in my case SDCard/MGMapsCache.</li>
		<li>Select Settings/Map/Map types, select options/add custom
			map,in map type name enter the name of the map you created using MAC
			in my case macos, map type url you can leave blank, select
			ok/options/save MGMaps will then apply the settings and display your
			created map.</li>
	</ol>
	<h4>Warning</h4>
	<p>Avoid using names native to MGMaps such as google, each name
		used must be defined as a custom map so the directory structure below
		must have macos,macroad and macsat defined as custom map types.</p>
	<pre>
MGMapsCache MGMapsCache\cache.conf MGMapsCache\macos_10
MGMapsCache\macos_11 MGMapsCache\macroad_11 MGMapsCache\macsat_11
MGMapsCache\macos_12 MGMapsCache\macroad_12 MGMapsCache\macsat_12
</pre>
	<!-- *************************************************************************** -->
	<h3>
		<a name="MTE">Creating and using atlases with Mobile Trail
			Explorer (MTE)</a>
	</h3>
	<p>
		For creating atlases compatible with Mobile Trail Explorer you have to
		select <b>Mobile Trail Explorer Cache</b> as format in atlas format
		selection dialog that appears when starting a new atlas (menu <b>Atlas</b>
		entry <b>New Atlas</b>).<br> If a map source uses an image format
		different to PNG the tiles will be automatically converted to the PNG
		format.<br> The output is one
		<tt>MTEFileCache</tt>
		file per atlas which contains all maps. An existing cache file can not
		be updated. If you want to add maps to an existing
		<tt>MTEFileCache</tt>
		please use the atlas format <b>Mobile Trail Explorer</b> which creates
		a file structure identical to JTileDownloader and then process the
		maps using <a
			href="http://code.google.com/p/mobile-trail-explorer/wiki/CacheCreator">MTE
			CacheCreator</a>.<br> As atlases for Mobile Trail Explorer does not
		support all features provided by Mobile Atlas Creator the following
		settings are ignored when creating atlases for Mobile Trail Explorer:
	</p>
	<ul>
		<li>Recreate/adjust map tiles (custom tile size and image format)</li>
		<li>Name of all layers and maps</li>
		<li>Structure of the atlas (which maps belongs to which layer)</li>
	</ul>
	<!-- *************************************************************************** -->
	<h3>
		<a name="NaviComputer">Creating atlases for NaviComputer</a>
	</h3>
	<p>
		For creating atlases, compatible with NaviComputer, you have to select
		<b>NaviComputer (NMAP)</b> as format in atlas format selection dialog
		that appears when starting a new atlas (menu <b>Atlas</b> entry <b>New
			Atlas</b>).<br> After defining the maps and layers for the atlas to
		be created, start atlas download and creation via the button <b>Create
			Atlas</b>. Once download and creation has completed, the generated file
		with the extension nmap can be found in the MOBAC output directory.
		This *.nmap-file is the required input file for NaviComputer.
	</p>
	<!-- *************************************************************************** -->
	<h3>
		<a name="nfComPass">Creating atlases for nfComPass</a>
	</h3>
	<p>
		For creating atlases, compatible with <a
			href="http://www.navifriends.com/phpbbForum/viewtopic.php?f=3&amp;t=17004">nfComPass</a>,
		you have to click <b>Atlas -> New Atlas</b>, select <b>nfComPass</b>
		and give your Atlas a name.<br> By default atlases with a
		tilesize of 64x64 are created (recommended). For different tile sizes
		check <b>Recreate/adjust map tiles (CPU intensive)</b> under Layer
		settings. Set Tileformat can not be changed - it is always png. Maybe
		you must tryout, what is the best tilesize for your device. Choose
		your layer and zoomlevels and click <b>Add selection</b>. Then click <b>Create
			atlas</b>. Once download and creation has completed, the generated
		folders can be found in the MOBAC output directory. You must copy the
		data from the
		<tt>nfComPass.dat</tt>
		to your nfComPass.dat and fill in the path to your mapdirectory. After
		that, copy the folder(s) to your device. If it is possible, you should
		not copy the files with Active Sync to your device.
	</p>
	<!-- *************************************************************************** -->
	<h3>
		<a name="OruxMaps">Creating OruxMaps atlases</a>
	</h3>
	<p>
		For creating atlases compatible with <a href="http://www.oruxmaps.com">OruxMaps</a>
		as format you have to select <b>OruxMaps</b> as format in atlas format
		selection dialog that appears when starting a new atlas (menu <b>Atlas</b>
		entry <b>New Atlas</b>).
	</p>
	<p>Using this atlas output format the following features are
		ignored when creating atlases:</p>
	<ul>
		<li>Layer settings, custom tile size. OruxMaps always uses
			512x512 tile size. You can select the tile format (PNG or JPEG). If
			you do not select any, default value is JPEG - quality 90.</li>
	</ul>
	<p>The output format of an "atlas" for OruxMaps is one or more map
		directories in the atlas directory. You have to copy those maps onto
		your device (default directory: /oruxmaps/mapfiles/).</p>
	<!-- *************************************************************************** -->
	<h3>
		<a name="OSMAND">Creating atlases for OSMAND</a>
	</h3>
	<p>
		For creating atlases compatible with OSMAND you have to select <b>OSMAND
			tile storage</b> or <b>OSMAND SQlite</b> as format in atlas format
		selection dialog that appears when starting a new atlas (menu <b>Atlas</b>
		entry <b>New Atlas</b>).<br> As atlases for OSMAND do not support
		all features provided by Mobile Atlas Creator the following settings
		are ignored when creating atlases for OSMAND:
	</p>
	<ul>
		<li>Change height or width of the map tiles</li>
		<li>Name of all layers and maps</li>
		<li>Structure of the atlas (which maps belongs to which layer)</li>
	</ul>
	<!-- *************************************************************************** -->
	<h3>
		<a name="Osmdroid">Creating atlases for Osmdroid</a>
	</h3>
	<p>
		For creating atlases compatible with Osmdroid you have to select
		either <b>Osmdroid ZIP</b>, <b>Osmdroid SQLite</b> or <b>Osmdroid
			GEMF</b> as format in atlas format selection dialog that appears when
		starting a new atlas (menu <b>Atlas</b> entry <b>New Atlas</b>).<br>
		The mentioned three formats are &quot;single file&quot; atlases. One
		of the other possible atlas formats might also be acceptable for
		Osmdroid. Also, there is other software that is able to deal with GEMF
		archives.<br> As atlases for Osmdroid do not support all features
		provided by Mobile Atlas Creator the following settings are ignored
		when creating atlases for Osmdroid:
	</p>
	<ul>
		<li>Change height or width of the map tiles</li>
		<li>Name of all layers and maps</li>
		<li>Structure of the atlas (which maps belongs to which layer)</li>
	</ul>
	<!-- *************************************************************************** -->
	<h3>
		<a name="OSMTracker">Creating atlases for OSMTracker</a>
	</h3>
	<p>
		For creating atlases compatible with OSMTracker you have to select <b>OSMTracker
			tile storage</b> as format in atlas format selection dialog that appears
		when starting a new atlas (menu <b>Atlas</b> entry <b>New Atlas</b>).<br>
		As atlases for OSMTracker do not support all features provided by
		Mobile Atlas Creator the following settings are ignored when creating
		atlases for OSMTracker:
	</p>
	<ul>
		<li>Change height or width of the map tiles</li>
		<li>Name of all layers and maps</li>
		<li>Structure of the atlas (which maps belongs to which layer)</li>
	</ul>
	<!-- *************************************************************************** -->
	<h3>
		<a name="Ozi">Creating and using atlases with OziExplorer / large
			PNG image export</a>
	</h3>
	<p>
		For creating atlases compatible with OziExplorer you have to select <b>OziExplorer
			(PNG &amp; MAP)</b> as format in atlas format selection dialog that
		appears when starting a new atlas (menu <b>Atlas</b> entry <b>New
			Atlas</b>).
	</p>
	<h4>
		<a name="OziRestriction">Restrictions</a>
	</h4>
	<p>As OziExplorer does not support tiled maps some features are
		ignored when creating atlases in this format:</p>
	<ul>
		<li>Image output format is fix: 24bit PNG</li>
		<li>Recreate/adjust map tiles custom tile is ignored</li>
	</ul>
	<p>
		The output format of an "atlas" for OziExplorer is one subdirectory
		per layer and within this subdirectory one
		<tt>PNG</tt>
		image and one
		<tt>MAP</tt>
		file per defined map. For opening a map in OziExplorer select the menu
		<b>File</b> &rarr; <b>Load from File</b> &rarr; <b>Load from MAP
			file</b>, browse to the layer directory of the created atlas and select
		the MAP file.
	</p>
	<p>If you are only interested in the map image you can safely
		delete the created map file.</p>
	<h4>
		<a name="OziWarning">Warning</a>
	</h4>
	<p>Mobile Atlas Creator uses a highly sophisticated and optimized
		algorithm for creating the PNG files for OziExplorer use. This
		algorithm allows to create very large maps images at low memory usage.
		OziExplorer and most image viewers do not use such sophisticated
		algorithms which can lead to the situation that you can create very
		large map images - but OziExplorer and other image viewers are not
		able to open the image.</p>
	<!-- *************************************************************************** -->
	<h3>
		<a name="PathAway">Creating atlases for PathAway</a>
	</h3>
	<p>
		For creating atlases compatible with PathAway you have to select <b>PathAway
			tile cache</b> as format in atlas format selection dialog that appears
		when starting a new atlas (menu <b>Atlas</b> entry <b>New Atlas</b>).
		<br> As atlases for PathAway do not support all features provided
		by Mobile Atlas Creator the following restrictions apply when creating
		atlases for PathAway:
	</p>
	<ul>
		<li>The maximum zoom level is 16 - higher zoom levels are not
			possible with this atlas format</li>
		<li>Tile width and width can not be changed (settings will be
			ignored)</li>
		<li>Name of all layers and maps is ignored</li>
		<li>Structure of the atlas is ignored (which maps belongs to
			which layer)</li>
	</ul>
	<!-- *************************************************************************** -->
	<h3>
		<a name="RMaps">Creating and using atlases with RMaps</a>
	</h3>
	<p>
		For creating offline atlases compatible with <a
			href="http://robertdeveloper.blogspot.com/search/label/rmaps">RMaps</a>
		(Android application) you have to select <b>RMaps SQLite</b> as format
		in atlas format selection dialog that appears when starting a new
		atlas (menu <b>Atlas</b> entry <b>New Atlas</b>).<br> The atlas
		format RMaps does not support all features provided by Mobile Atlas
		Creator the following settings can not be used or are ignored when
		creating atlases using this output format:
	</p>
	<ul>
		<li>Recreate/adjust map tiles with custom tile size (height and
			width have to be 256)</li>
		<li>Name of all layers and maps</li>
		<li>Structure of the atlas (which maps belongs to which layer)</li>
		<li>Atlases created after another are merged into one Database
			named <tt>[AtlasName] atlas.sqlitedb</tt> which is located in the
			atlas output directory.
		</li>
	</ul>
	<!-- *************************************************************************** -->
	<h3>
		<a name="SportsTracker">[Nokia] Sports Tracker</a>
	</h3>
	<p>
		For creating atlases compatible with <a
			href="http://www.sports-tracker.com">Sports Tracker(ST)</a> you have
		to select <b>Sports Tracker</b> (NOT GPS Sportstracker) as format in
		atlas format selection dialog that appears when starting a new atlas
		(menu <b>Atlas</b> entry <b>New Atlas</b>).
	</p>
	<p>
		Do not select <b>Recreate/adjust map tiles</b>.
	</p>
	<p>Maximum Zoomlevel of Sports Tracker is 17, default is 13.</p>
	<p>Copy the created atlas (the whole folder) into the following
		folder of youre phone (depending of the Sports Tracker version):</p>
	<ul>
		<li>Sports Tracker 1.76: <tt>E:\system\data\Maps\Street\</tt></li>
		<li>Sports Tracker 2.x: <tt>E:\system\data\Maps\Street\</tt></li>
		<li>Sports Tracker 3.x: <tt>E:\system\data\STMaps\Street\</tt></li>
	</ul>
	<p>For changing the zoom level inside Storts Tracker press 5 to
		zoom in and 0 to zoom out.</p>

	<!-- *************************************************************************** -->
	<h3>
		<a name="TTQV">Creating and using atlases with Touratech QV /
			large PNG image export</a>
	</h3>
	<p>
		For creating atlases compatible with Touratech QV you have to select <b>Touratech
			QV</b> as format in atlas format selection dialog that appears when
		starting a new atlas (menu <b>Atlas</b> entry <b>New Atlas</b>).
	</p>
	<h4>
		<a name="TTQVRestriction">Restrictions</a>
	</h4>
	<p>As Touratech QV does not support tiled maps some features are
		ignored when creating atlases in this format:</p>
	<ul>
		<li>Image output format is fix: 24bit PNG</li>
		<li>Recreate/adjust map tiles custom tile is ignored</li>
	</ul>
	<p>
		The output format of an "atlas" for Touratech QV is one subdirectory
		per layer and within this subdirectory one
		<tt>PNG</tt>
		image and one
		<tt>CAL</tt>
		file per defined map.
	</p>
	<p>If you are only interested in the map image you can safely
		delete the created cal file.</p>
	<h4>
		<a name="TTQVWarning">Warning</a>
	</h4>
	<p>Mobile Atlas Creator uses a highly sophisticated and optimized
		algorithm for creating the PNG files for Touratech QV use. This
		algorithm allows to create very large maps images at low memory usage.
		Touratech QV and most image viewers do not use such sophisticated
		algorithms which can lead to the situation that you can create very
		large map images - but Touratech QV and other image viewers are not
		able to open the image.</p>
	<!-- *************************************************************************** -->
	<h3>
		<a name="TomTomRaster">Creating atlases using TomTom Raster format</a>
	</h3>
	<p>TBD</p>
	<!-- *************************************************************************** -->
	<h3>
		<a name="TrekBuddy">Creating and using atlases with TrekBuddy</a>
	</h3>
	<p>
		For creating atlases compatible with TrekBuddy you have to select <b>TrekBuddy
			tared atlas</b> or <b>TrekBuddy untared atlas</b> as format in atlas
		format selection dialog that appears when starting a new atlas (menu <b>Atlas</b>
		entry <b>New Atlas</b>).
	</p>
	<p>
		After defining the maps and layers for the atlas to be created start
		atlas download and creation via the button <b>Create Atlas</b>. Once
		atlas download and creation has completed all necessary files
		belonging to the atlas can be found in the directory
		<tt>atlases\[atlas name]_[current date and time]</tt>
		.
	</p>
	<p>
		The atlas itself consists of the atlas startup file
		<tt>cr.tar</tt>
		(tar format) or
		<tt>cr.tba</tt>
		(regular/untared format) and the subdirectories containing the
		different maps of the atlas. For using the atlas with TrekBuddy copy
		the whole directory onto your J2ME device. Then use the <b>Load
			Atlas</b> function of TrekBuddy and open
		<tt>cr.tar</tt>
		/
		<tt>cr.tba</tt>
		(in the atlas root directory).
	</p>
	<!-- *************************************************************************** -->
	<h3>
		<a name="TwoNav">Creating and using atlases with TwoNav &amp;
			CompeGPS Land/Air</a>
	</h3>
	<p>
		To create atlases compatible with TwoNav software you have to select <b>TwoNav
			(RMAP)</b> as format in atlas format selection dialog that appears when
		starting a new atlas (menu <b>Atlas</b> entry <b>New Atlas</b>).
		Atlases created for TwoNav are stored in a format called rmap. It's a
		binary format that holds the same map data stored at different
		resolutions - in order to make zooming in and out on low performance
		mobile devices fast and efficient. However, this causes some
		restrictions which have to be taken into account:
	</p>
	<ul>
		<li>Each map within a layer has to have the same geographical
			bounds.</li>
		<li>There only can be one map in a layer with a given zoom level</li>
	</ul>
	<p>If there are several layers in one atlas, each layer will be
		stored as a separate rmap file.</p>
	<p>The easiest way to create a correct atlas content is: first
		select the appropriate grid zoom (combobox next to the zoom slider),
		then pick zoom levels from the selected grid zoom up to the zoom level
		of the desired most detailed level, and finally add a selection to the
		Atlas content by clicking on the "Add selection" button.</p>
	<p>Rmap format also requires no gaps in a zoom level range from the
		maximum to the minimum selected zoom level. If there are missing zoom
		levels, they will be created internally by shrinking the existing
		downloaded tiles. If the missing zoom levels contain a lot of tiles,
		this operation could take a while.</p>
	<p>
		Finally copy the
		<tt>layer.rmap</tt>
		file from the
		<tt>atlases\[atlas name]_[current date and time]</tt>
		folder to your TwoNav
		<tt>maps</tt>
		folder.
	</p>
	<p>As TwoNav does not support all available features provided my
		MOBAC, some features can not be used when creating atlases in this
		format:</p>
	<ul>
		<li>Custom tile height and width (is ignored for TwoNav RMP
			atlases)</li>
		<li>Custom tile format: Only JPEG formats are allowed</li>
	</ul>
	<!-- *************************************************************************** -->
	<h3>
		<a name="Viewranger">Creating and using atlases with Viewranger</a>
	</h3>
	<p>
		For creating atlases compatible with <a
			href="http://www.viewranger.com/">Viewranger(VR)</a> you have to
		select <b>Viewranger</b> as format in atlas format selection dialog
		that appears when starting a new atlas (menu <b>Atlas</b> entry <b>New
			Atlas</b>).
	</p>
	<p>Maximum Zoomlevel of Viewranger is 18, minimum is 3.</p>
	<p>After creating youre atlas the folder structure looks like:</p>
	<ul>
		<li><tt>Mobile Atlas Creator
				1.9\atlases\VR_2012-03-28_154944\OSM\13\4308</tt></li>
		<li><tt>Mobile Atlas Creator
				1.9\atlases\VR_2012-03-28_154944\OSM\14\43</tt></li>
		<li><tt>Mobile Atlas Creator
				1.9\atlases\VR_2012-03-28_154944\google\13\4308</tt></li>
		<li><tt>Mobile Atlas Creator
				1.9\atlases\VR_2012-03-28_154944\google\14\43</tt></li>
	</ul>
	<p>
		Now we have to <a
			href="http://support.viewranger.com/wikihelp/index.php/Map_cache_structure">
			Create a Folder Structure on the Device:</a>
	</p>
	<P>
		If you youre VR Folder is on E: it is on Symbian located in
		<tt>E:/ViewRanger/MapCache/_PAlbTN/</tt>
	</P>
	<P>In this folder create following Subfolders, if not already
		present:</P>
	<P>84,85,87,88,89,129</P>
	<P>
		e.g.
		<tt>/ViewRanger/MapCache/_PAlbTN/84</tt>
	</p>
	<p>Copy the content of "OSM" into 84, "google" into 85 and so on.</p>
	<p>
		Now it looks like:
		<tt>E:/ViewRanger/MapCache/_PAlbTN/13/4308/2687</tt>
		, 2687 is a tile
	</p>
	<p>VR has different Online Mapsources which are assigned to the
		Numbers as shown:</p>

	<ul>
		<li><tt>OSM-&gt;84</tt></li>
		<li><tt>Opencyclemap-&gt;85</tt></li>
		<li><tt>OSM Direct-&gt;87</tt></li>
		<li><tt>OSM Midnigth-&gt;88</tt></li>
		<li><tt>OSM Fresh-&gt;89</tt></li>
		<li><tt>Open Piste Map-&gt;129 </tt></li>
	</ul>

	<p>Of course you can fill the Tilecache with different Maps.</p>
	<p>I use the Open Piste Map eg. as "OSM Public Transport"</p>

	<!-- *************************************************************************** -->
	<h2>
		<a name="Enhancement">Enhancement requests</a>
	</h2>
	<p>
		If you are missing the map provider of your choice or have other
		enhancement ideas for Mobile Atlas Creator feel free to open an <a
			href="http://sourceforge.net/tracker/?group_id=238075&amp;atid=1105497">Feature
			Request Ticket</a> at SourceForge.
	</p>
	<p>
		If have a new online map which is not available in Mobile Atlas
		Creator there my be change to add it. Before opening a Feature Request
		please take a look into the <a
			href="http://svn.code.sf.net/p/mobac/code/tags/MOBAC%202.0/v2.0.0%20beta%203/misc/Incompatible%20maps.txt">list
			of map sources known to incompatible with Mobile Atlas Creator</a>.
	</p>

	<!-- *************************************************************************** -->
	<h2>
		<a name="Bugs">Problems, Bugs &amp; Errors</a>
	</h2>
	<p>
		In case of unexpected errors while executing Mobile Atlas Creator you
		may get presented a exception dialog containing detailed information
		about the problem. In such a case please create a new <a
			href="http://sourceforge.net/tracker/?group_id=238075&amp;atid=1105494">ticket
			in the Bug Tracker</a> at SourceForge. Please add the detailed exception
		information and a detailed description of your last performed actions.
	</p>

	<h3>The default error log</h3>
	<p>
		By default Mobile Atlas Creator records all errors of the current
		session into it's error log file
		<tt>Mobile Atlas Creator.log</tt>
		. This log file is located on Windows system in the directory
		<tt>%APPDATA%\Mobile Atlas Creator\</tt>
		and on Linux/Unix/OSX system in the directory
		<tt>~/.mobac/</tt>
	</p>

	<h3>Activate the advanced logging system</h3>
	<p>
		If the recorded errors in the error log do not indicate a problem you
		can activate the overall message logging mechanism of Mobile Atlas
		Creator:<br> Download the file <a
			href="http://mobac.sourceforge.net/log4j.xml">log4j.xml</a> and save
		it in the directory where the jar file of Mobile Atlas Creator is
		installed to.
	</p>
	<p>
		The next start Mobile Atlas Creator will create a log file in the
		current directory (on Windows this is usually the directory where the
		JAR file is located on Linux usually the profile directory). Please
		note that the log file is erased on each program start. If you think
		you have found a bug please file it in the <a
			href="http://sourceforge.net/tracker/?group_id=238075&amp;atid=1105494">bug
			tracker at SourceForge</a>.
	</p>

	<!-- *************************************************************************** -->
	<h2>
		<a name="Limitations">Known problems and limitations</a>
	</h2>
	<h3>New map sources</h3>
	<p>
		Mobile Atlas Creator is limited to map sources that provide their maps
		if form of map tiles. Each of that map tiles has to be of size 256x256
		pixels. Additionally the map source has to use the spherical Mercator
		projection and the number of tiles forming the world on each zoom
		level has to be one of the following values: 2<sup>0</sup>, 2<sup>1</sup>,
		2<sup>2</sup> ... 2<sup>21</sup>, 2<sup>22</sup>.<br> For more
		details see OpenStreetMap Wiki: <a
			href="http://wiki.openstreetmap.org/wiki/Slippy_map_tilenames">Slippy
			map tilenames</a>, <a href="http://wiki.openstreetmap.org/wiki/Mercator">Mercator</a>,
		<a href="http://wiki.openstreetmap.org/wiki/Height_and_width_of_a_map">Height
			and width of a map</a> and <a
			href="http://wiki.openstreetmap.org/wiki/Zoom_levels">Zoom levels</a>
	</p>
	<h3>Java Bugs</h3>
	<p>Due to bugs in Java you should not do the following:</p>
	<ul>
		<li>Install Mobile Atlas Creator into a directory which path
			contains an "!" (exclamation mark) because of this <a
			href="http://bugs.sun.com/view_bug.do?bug_id=4523159">Sun Java
				bug</a>
		</li>
		<li>Do not use OpenJDK if you want to work with GPX tracks in
			Mobile Atlas Creator</li>
		<li>On Windows without a system proxy set (see connection
			settings of IE) it is strongly recommended <b>not to use</b> the
			following proxy setting:<i>Use standard Java proxy settings</i>
	</ul>

	<!-- *************************************************************************** -->
	<h2>
		<a name="AdvancedUsers">Details for advanced users</a>
	</h2>
	<h3>
		<a name="DirectoryConfig">Specifying directory configuration</a>
	</h3>
	<p>The following steps are necessary if MOBAC is installed to to a
		directory that is not writable for reguar users:</p>
	<p>
		For changing the directory configuration pattern for all users of a
		MOBAC installation save <a
			href="http://svn.code.sf.net/p/mobac/code/tags/MOBAC%202.0/v2.0.0%20beta%203/directories.ini.template">this
			file</a> into the same directory where
		<tt>Mobile_Atlas_Creator.jar</tt>
		has been installed into and change it's name to
		<tt>directories.ini</tt>
		. For more details read the comments in this configuration file.
	</p>

	<h3>
		<a name="TileStoreDir">Moving the tile store directory</a>
	</h3>
	<p>
		Usually the tile store directory where Mobile Atlas Creator saves all
		downloaded images in is automatically determined.<br> In case you
		want to select a different directory perform the following steps:
	</p>
	<ol>
		<li>Make sure you have closed MOBAC</li>
		<li>Open <tt>settings.xml</tt> in an text editor
		</li>
		<li>Inside of the tag <tt>&lt;settings&gt;</tt> search for the
			tag <tt>&lt;directories&gt;</tt>. Inside this tag create a new tag
			named <tt>&lt;tileStoreDirectory&gt;</tt></li>
		<li>Set the path name to the value of this tag (Windows users
			should replace backslashes with a slashes)</li>
		<li>(optional) Copy or move the content of the old tile store
			directory into the new tile store directory.</li>
	</ol>
	<h4>Example</h4>
	<pre>
&lt;settings&gt;
    &lt;directories&gt;
        &lt;tileStoreDirectory&gt;E:/tiles&lt;/tileStoreDirectory&gt;
    &lt;/directories&gt;
    ...
&lt;/settings&gt;</pre>
	<p>
		This specified the windows directory
		<tt>E:\tiles</tt>
		as new tile store directory. The previously used tile store will not
		be used anymore.<br> Deleting the
		<tt>&lt;tileStoreDirectory&gt;</tt>
		tag restores the old behavior (automatically tile store directory
		selection).
	</p>

	<h3>
		<a name="ExternalTools">Starting external tools from within MOBAC</a>
	</h3>

	<p>
		External tools like scripts or other executable programs can be
		started from the <b>Tools</b> menu from within MOBAC. This menu is
		only visible if external programs have been configured. The advantage
		of starting a program from within MOBAC is that certain information
		about selected map source, selected region ... can be transmitted as
		parameters to the executed program.<br> This allows you for
		example to create your own maps (render tiles) with external tools
		like <a href="http://wiki.openstreetmap.org/wiki/Osmfilter">OSMFILTER</a>,
		<a href="http://wiki.openstreetmap.org/wiki/Osmconvert">OSMCONVERT</a>,
		<a href="http://maperitive.net/">MAPERITIVE</a>...
	</p>
	<p>
		For defining an external program, create an xml file for each external
		program to be called. The content of the xml file has to be like one
		of the following examples. The file-name of the xml is not relevant -
		it only has to end with
		<tt>.xml</tt>
	<h4>test.xml</h4>
	<p>Demonstrates how to execute an Windows batch file.</p>
	<pre>
&lt;?xml version=&quot;1.0&quot; encoding=&quot;UTF-8&quot; standalone=&quot;yes&quot;?&gt;
&lt;ExternalTool&gt;
 &lt;name&gt;Name shown in tools menu&lt;/name&gt;
 &lt;command&gt;cmd.exe /c start .\tools\mybatch.cmd&lt;/command&gt;
 &lt;parameters&gt;MIN_LON MIN_LAT MAX_LON MAX_LAT MIN_ZOOM MAX_ZOOM MAPSOURCE_NAME MAPSOURCE_DISPLAYNAME NAME_EDITBOX &lt;/parameters&gt;
 &lt;debug&gt;true&lt;/debug&gt;
&lt;/ExternalTool&gt;
</pre>
	<p>
		<a
			href="http://svn.code.sf.net/p/mobac/code/tags/MOBAC%202.0/v2.0.0%20beta%203/tools/test.xml">Annotated
			sample file download</a>
	</p>

	<h4>test-exe.xml</h4>
	<p>Demonstrates how to execute an regular windows program.</p>
	<pre>
&lt;?xml version=&quot;1.0&quot; encoding=&quot;UTF-8&quot; standalone=&quot;yes&quot;?&gt;
&lt;ExternalTool&gt;
 &lt;name&gt;Name shown in tools menu&lt;/name&gt;
 &lt;command&gt;C:\sample-path\program.exe&lt;/command&gt;
 &lt;parameters&gt;MIN_LON MIN_LAT MAX_LON MAX_LAT MIN_ZOOM MAX_ZOOM MAPSOURCE_NAME MAPSOURCE_DISPLAYNAME NAME_EDITBOX &lt;/parameters&gt;
 &lt;debug&gt;true&lt;/debug&gt;
&lt;/ExternalTool&gt;
</pre>

	<p>
		The most interesting section is the content of <b>&lt;parameters&gt;</b>.
		It contains a space separated list of parameters the specified command
		will be executed with. The following values can be used:
	<ul>
		<li><tt>MAX_LAT</tt> - Maximum latitude (upper border) off the
			selected area</li>
		<li><tt>MIN_LAT</tt> - Minimum latitude (lower border) off the
			selected area</li>
		<li><tt>MAX_LON</tt> - Maximum longitude (right border) off the
			selected area</li>
		<li><tt>MIN_LON</tt> - Minimum longitude (left border) off the
			selected area</li>
		<li><tt>MIN_ZOOM</tt> - minimum zoom of selected zoom levels
			check-boxes</li>
		<li><tt>MAX_ZOOM</tt> - maximum zoom of selected zoom levels
			check-boxes</li>
		<li><tt>MAPSOURCE_NAME</tt> - Currently select map source
			internal name (used in atlas profile xml file)</li>
		<li><tt>MAPSOURCE_DISPLAYNAME</tt> - Currently select map source
			display name (as shown in the GUI)</li>
		<li><tt>NAME_EDITBOX</tt> - content of the edit box "Name" in the
			side panel "Atlas Content"
	</ul>


	<!-- *************************************************************************** -->
	<h2>
		<a name="CustomMapSource">Custom map sources</a>
	</h2>
	<h3>
		<a name="SimpleCustomMapSource">Simple custom map sources</a>
	</h3>
	<p>
		Custom map sources which uses a similar URL scheme as
		Google/OpenStreetMap can be added by saving for each custom map source
		the definition in form of an xml file in the
		<tt>mapsources</tt>
		directory.
	</p>
	<p>The following section shows is an example how the xml file has
		to be formatted. It defines an additional map source named "Custom OSM
		Mapnik" which shows map tiles identical to the predefined map source
		"OpenStreetMap Mapnik".</p>
	<p>
		<a name="MapSourceNameUnique"></a><b>Note:</b>The name specified in
		there has to be unique among all available map sources within MOBAC.
		The list of all available map sources can be obtained via command <b>Show
			all map source names</b> in the menu <b>Debug</b>.
	</p>
	<pre>
&lt;?xml version=&quot;1.0&quot; encoding=&quot;UTF-8&quot;?&gt;
&lt;customMapSource&gt;
	&lt;name&gt;Custom OSM Mapnik&lt;/name&gt;
	&lt;minZoom&gt;0&lt;/minZoom&gt;
	&lt;maxZoom&gt;18&lt;/maxZoom&gt;
	&lt;tileType&gt;png&lt;/tileType&gt;
	&lt;tileUpdate&gt;None&lt;/tileUpdate&gt;
	&lt;url&gt;http://tile.openstreetmap.org/{$z}/{$x}/{$y}.png&lt;/url&gt;
	&lt;backgroundColor&gt;#000000&lt;/backgroundColor&gt;
&lt;/customMapSource&gt;
</pre>
	<p>The most important part of this definition is the url. It is a
		template containing specific placeholders which are encapsulated by
		curly brace:</p>
	<ul>
		<li><b>{$z}</b> for the zoom level - number range: [<i>minZoom</i>
			.. <i>maxZoom</i>]</li>
		<li><b>{$x}</b> for the x tile coordinate - number range: [0..2<sup><i>zoom
					level</i> </sup>]</li>
		<li><b>{$y}</b> for the y tile coordinate - number range: [0..2<sup><i>zoom
					level</i> </sup>]</li>
	</ul>
	<p>
		Note: If the url contains the ampersand character <b>&amp;</b> you
		have to encode it as <b>&amp;amp;</b>. Otherwise it not be valid XML
		and therefore can not bo loaded by MOBAC.
	</p>
	<p>
		Example file for download: <a
			href="http://svn.code.sf.net/p/mobac/code/tags/MOBAC%202.0/v2.0.0%20beta%203/mapsources/Example%20custom%20map%20source.xml">
			Example custom map source.xml</a>
	</p>
	<h3>
		<a name="CustomWMSMapSource">Custom WMS map sources</a>
	</h3>
	<p>
		Similar a WMS map source can be defined. Currently only
		<tt>EPSG:4326</tt>
		as coordinatesystem is supported.
	</p>
	<pre>&lt;?xml version="1.0" encoding="UTF-8" standalone="yes"?&gt;
&lt;customWmsMapSource&gt;
    &lt;name&gt;TerraServer WMS&lt;/name&gt;
    &lt;minZoom&gt;12&lt;/minZoom&gt;
    &lt;maxZoom&gt;18&lt;/maxZoom&gt;
    &lt;tileType&gt;JPG&lt;/tileType&gt;
    &lt;version&gt;1.1.1&lt;/version&gt;
    &lt;layers&gt;DRG&lt;/layers&gt;
    &lt;url&gt;http://terraserver-usa.com/ogcmap6.ashx?&lt;/url&gt;
    &lt;coordinatesystem&gt;EPSG:4326&lt;/coordinatesystem&gt;
    &lt;aditionalparameters&gt;&amp;amp;EXCEPTIONS=BLANK&amp;amp;Styles=&lt;/aditionalparameters&gt;
    &lt;backgroundColor&gt;#000000&lt;/backgroundColor&gt;
&lt;/customWmsMapSource&gt;</pre>
	<p>
		Example file (with comments) for download: <a
			href="http://svn.code.sf.net/p/mobac/code/tags/MOBAC%202.0/v2.0.0%20beta%203/mapsources/Example%20custom%20WMS%20map%20source.xml">
			Example custom WMS map source.xml</a>
	</p>
	<h3>
		<a name="CustomMultiLayerMapSource">Custom multi-layer map sources</a>
	</h3>
	<p>
		The same way as <a href="#CustomMapSource">custom map sources</a> map
		sources which consist of two or more layers can be defined as well.
		Note that all except the background map source layer (first in the
		list) must have transparent parts - otherwise layers in the list
		before will not be visible.
	</p>
	<pre>
&lt;?xml version=&quot;1.0&quot; encoding=&quot;UTF-8&quot; standalone=&quot;yes&quot;?&gt;
&lt;customMultiLayerMapSource&gt;
    &lt;name&gt;Custom OSM Mapnik with Hills (Ger)&lt;/name&gt;
    &lt;tileType&gt;PNG&lt;/tileType&gt;
    &lt;backgroundColor&gt;#000000&lt;/backgroundColor&gt;
    &lt;layers&gt;
        &lt;customMapSource&gt;
            &lt;name&gt;Custom OSM Mapnik&lt;/name&gt;
            &lt;minZoom&gt;0&lt;/minZoom&gt;
            &lt;maxZoom&gt;18&lt;/maxZoom&gt;
            &lt;tileType&gt;PNG&lt;/tileType&gt;
            &lt;tileUpdate&gt;None&lt;/tileUpdate&gt;
            &lt;url&gt;http://tile.openstreetmap.org/{$z}/{$x}/{$y}.png&lt;/url&gt;
        &lt;/customMapSource&gt;
        &lt;customMapSource&gt;
            &lt;name&gt;Custom transparent hillshade&lt;/name&gt;
            &lt;minZoom&gt;0&lt;/minZoom&gt;
            &lt;maxZoom&gt;18&lt;/maxZoom&gt;
            &lt;tileType&gt;PNG&lt;/tileType&gt;
            &lt;tileUpdate&gt;None&lt;/tileUpdate&gt;
            &lt;url&gt;http://www.wanderreitkarte.de/hills/{$z}/{$x}/{$y}.png&lt;/url&gt;
        &lt;/customMapSource&gt;
    &lt;/layers&gt;
&lt;/customMultiLayerMapSource&gt;
</pre>
	<p>
		Example file for download: <a
			href="http://svn.code.sf.net/p/mobac/code/tags/MOBAC%202.0/v2.0.0%20beta%203/mapsources/Example%20custom%20multi-layer%20map%20source.xml">
			Example custom multi-layer map source.xml</a>
	</p>
	<h3>
		<a name="CloudMadeMapSource">Custom CloudMade map sources</a>
	</h3>
	<p>
		The <a href="http://maps.cloudmade.com/">CloudMade map service</a>
		offers a large number of OpenStreetMap based maps with different
		styles. Each style is accessible through it's
		<tt>styleID</tt>
		. Custom CloudMade maps can be added to MOBAC via a simple XML file
		containing a map name used by MOBAC and a styleID:
	</p>
	<pre>&lt;?xml version=&quot;1.0&quot; encoding=&quot;UTF-8&quot; standalone=&quot;yes&quot;?&gt;
&lt;cloudMade&gt;
    &lt;displayName&gt;CloudMade blackout&lt;/displayName&gt;
    &lt;styleID&gt;1960&lt;/styleID&gt;
&lt;/cloudMade&gt;</pre>
	<p>
		Example file for download: <a
			href="http://svn.code.sf.net/p/mobac/code/tags/MOBAC%202.0/v2.0.0%20beta%203/mapsources/Example%20CloudMade1960.xml">
			Example CloudMade1960.xml</a>
	</p>
	<h3>
		<a name="BeanShellMapSource">Custom BeanShell map sources</a>
	</h3>
	<p>
		BeanShell map sources as the can be developed using <a
			href="http://sourceforge.net/apps/mediawiki/mobac/index.php?title=MapEvaluator">MapEvaluator</a>
		can be used by MOBAC. To do so place the saved BeanShell code file
		(file extension
		<tt>.bsh</tt>
		) in the
		<tt>mapsources</tt>
		directory. It will be loaded on next start-up of MOBAC.
	</p>
	<p>
		It is recommended to add a line defining the map source name (<a
			href="#MapSourceNameUnique">must be unique</a>).
	</p>
	<pre>name = "Your map source name here";</pre>
	<p>
		Example file for download: <a
			href="http://svn.code.sf.net/p/mobac/code/tags/MOBAC%202.0/v2.0.0%20beta%203/mapsources/Example%20beanshell%20map%20source.bsh">
			Example beanshell map source.bsh</a>
	</p>

	<h3>
		<a name="CustomMapPack">Custom Map Pack</a>
	</h3>
	<p>
		Developing a custom map pack requires at least basic Java skills.
		Therefore the description on how to develop a custom map pack is only
		part of the source code release of MOBAC. You can get the source code
		of MOBAC by using the latest
		<tt>src</tt>
		release available in the <a
			href="http://sourceforge.net/projects/mobac/files/Mobile%20Atlas%20Creator/">files
			section at Sourceforge</a> or you can get it directly from the <a
			href="http://sourceforge.net/p/mobac/code/">Subversion code
			repository</a> using the latest
		<tt>trunk</tt>
		version.
	</p>
	<h3>
		<a name="Mapsforge">MOBAC integrated rendering of tiles based on
			OpenStreetmap (mapsforge) vector data</a>
	</h3>
	<p>
		Since version 2.0 MOBAC includes the <a
			href="https://code.google.com/p/mapsforge/">mapsforge</a> rendering
		engine. This allows MOBAC to render bitmap tiles on-the-fly using
		Mapsforge vector data files. Those vector data files can be <a
			href="http://download.mapsforge.org/maps/">downloaded</a>
		pre-generated for a large number of regions world-wide. Alternatively
		you can <a
			href="https://code.google.com/p/mapsforge/wiki/GettingStartedMapWriter">convert
			OpenStreetMap data to mapsforge format on your own</a>. The map rendering
		of the vector data can be configured using <a
			href="https://code.google.com/p/mapsforge/wiki/RenderThemeAPI">xml
			base render themes</a>.
	</p>
	<p>For using mapsforge vector data within MOBAC the following steps
		are required:</p>
	<ol>
		<li><a href="http://download.mapsforge.org/maps/">Download</a> or
			create a mapsforge vector data file and save it on your compurter</li>
		<li>Create a custom XML map source file in the <tt>mapsources</tt>
			subdirectory similar to the <a
			href="http://svn.code.sf.net/p/mobac/code/tags/MOBAC%202.0/v2.0.0%20beta%203/mapsources/Example custom mapsforge map source.xml">example
				file</a>. <pre>
&lt;?xml version=&quot;1.0&quot; encoding=&quot;UTF-8&quot;?&gt;
&lt;mapsforge&gt;
	&lt;!-- name of the map - as shown in map source list --&gt;
	&lt;name&gt;Custom Mapsforge&lt;/name&gt;
	
	&lt;!-- optional --&gt;
	&lt;minZoom&gt;0&lt;/minZoom&gt; 
	
	&lt;!-- optional --&gt;
	&lt;maxZoom&gt;20&lt;/maxZoom&gt; 
	    
	&lt;!-- absolute or relative file name --&gt;
	&lt;mapFile&gt;mapsforge-test.map&lt;/mapFile&gt;
	
	&lt;!-- optional default OSMARENDERER Theme --&gt;
	&lt;!-- &lt;xmlRenderTheme&gt;mytheme.xml&lt;/xmlRenderTheme&gt; --&gt;
	
	&lt;transparent&gt;false&lt;/transparent&gt;
	
	&lt;!-- text size scale factor --&gt;
	&lt;textScale&gt;1.0&lt;/textScale&gt;
	
&lt;/mapsforge&gt;
</pre>
		</li>
		<li>Start or Restart MOBAC</li>
	</ol>

	<h3>
		<a name="FileBased">Custom atlas as map source / locally generated
			tiles</a>
	</h3>
	<p>
		Existing atlases or locally rendered tiles can be directly integrated
		into MOBAC as custom map source without having to set-up a local
		web-server. <br> At the moment the formats used by OSMTracker,
		AndNav, Maverick and OSMAND are supported. For adding such an atlas as
		map source download the <a
			href="http://svn.code.sf.net/p/mobac/code/tags/MOBAC%202.0/v2.0.0%20beta%203/mapsources/Example%20custom%20tile%20files%20source.xml">Example
			custom tile files source.xml</a> file, adapt the
		<tt>&lt;sourceFolder&gt;</tt>
		entry and place it in the
		<tt>mapsources</tt>
		directory.
	</p>
	<p>
		Tiles can also be packed into one or more zip files and directly used
		by MOBAC. For details please see the <a
			href="http://svn.code.sf.net/p/mobac/code/tags/MOBAC%202.0/v2.0.0%20beta%203/mapsources/Example%20custom%20tile%20zip%20source.xml">Example
			custom tile zip source.xml</a>.<br> <b>Note: When working with
			large ZIP files (more than 4 GB) it is required to use Java 7.</b>
	</p>
	<p>
		SQLite based atlas formats (RMaps, MBTiles, BigPlanetTracks,
		NaviComputer or OSMAND) can also be used directly by MOBAC. For
		details please see the <a
			href="http://svn.code.sf.net/p/mobac/code/tags/MOBAC%202.0/v2.0.0%20beta%203/mapsources/Example%20custom%20tile%20SQLite%20source.xml">Example
			custom tile SQLite source.xml</a>
	</p>
</body>
</html>
