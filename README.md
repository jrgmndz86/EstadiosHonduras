<!DOCTYPE html>
<html>
    <p><b><font size = 6, color = "white">GEOVISOR / CTE-524 Programación Aplicada a Entornos de SIG </font>
	</br><br><font size = 5, color = "white"> JORGE MÉNDEZ CASTILLO - OGT100512 </font>
	</br><br><font size = 5, color = "white"> ESTADIOS CERTIFICADOS PARA JUEGOS DE LIGA NACIONAL DE HONDURAS </font>
	<body background="grama2.jpg" gbcolor= "FF7F50">
	
	<head>
		<meta charset="utf-8"/>
		<title>GEOVISOR/CTE-524/OGT100512</title>
	
		<link rel="stylesheet" href="https://unpkg.com/leaflet@1.5.1/dist/leaflet.css"
		integrity="sha512-xwE/Az9zrjBIphAcBb3F6JVqxf46+CDLwfLMHloNu6KEQCAWi6HcDUbeOfBIptF7tcCzusKFjFw2yuvEpDL9wQ=="
		crossorigin=""/>
		
	    <script src="https://unpkg.com/leaflet@1.5.1/dist/leaflet.js"
		integrity="sha512-GffPMF3RvMeYyc1LWMHtK8EbPv0iNZ8/oTtHPx9/cc2ILxQ+u905qIwdpULaqDkyBKgOaB57QTMg7ztg8Jm2Og=="
		crossorigin="">
		</script>
	
		<!--MiniMap-->
		<link rel="stylesheet" href="Control.MiniMap.css" />
		<script src="Control.MiniMap.js" type= "text/javascript">
		</script>
		
		<!--measurecontrol-->
		<link rel="stylesheet" href="leaflet-measure.scss" />
		<script src="leaflet.measurecontrol.js" type= "text/javascript">
		</script>
	
		<!--MousePosition-->
		<link rel="stylesheet" href="L.Control.MousePosition.css" />
		<script src="L.Control.MousePosition.js" type= "text/javascript">
		</script>
		
		<!--Google Search-->		
		<script async src="https://cse.google.com/cse.js?cx=014667652707368315001:ksuiyekipnq"></script>
		<div class="gcse-search"></div>
		
		<!--fullscreen-->
		<link rel='stylesheet' href='leaflet.fullscreen.css'  />
		<script src='Leaflet.fullscreen.min.js'></script>
		
		<!--viewcenter-->
		<link rel="stylesheet" href="leaflet.viewcenter.css" />
		<script src="leaflet.viewcenter.js"></script>
				
	</head>
	
	<body>
	    <div id="map" style="width: 1200px; height: 600px;"></div>
	    
		<marquee scrolldelay= "50" direction="down" collamount= "10" height = "500px"><center>
		
		<img src = "b215b5c48172927d7bf50218d686d2bc_XL.jpg"/>
		<img src = "dt.common.streams.StreamServer (1).jpg"/>
		<img src = "dt.common.streams.StreamServer.jpg"/>
		<img src = "ESTADIO.jpg"/>
		<img src = "62909908_XBqHZOuOEAHFsvON7s6w4wA4YmKQoHVjkbMEmw4fCM0.jpg"/>
		<img src = "ESTADIO-CHOLUTECA-3.jpg"/>
		<img src = "300px-Ruben_Guifarrostadium.jpg"/>
		<img src = "dt.common.streams.StreamServer (2).jpg"/>
		<img src = "CDD1T-sWAAAQLgi.jpg"/>
		
		<script>
		
		var osm = L.tileLayer('https://api.tiles.mapbox.com/v4/{id}/{z}/{x}/{y}.png?access_token={accessToken}', 
			{attribution: 'Map data &copy; <a href="https://www.openstreetmap.org/">OpenStreetMap</a> contributors,<a href="https://creativecommons.org/licenses/by-sa/2.0/">CC-BY-SA</a>, Imagery © <a href="https://www.mapbox.com/">Mapbox</a>', 
			id: 'mapbox.streets-satellite', 
			accessToken:'pk.eyJ1IjoianJnbW5keiIsImEiOiJjazA3YnJta3UwMnRoM21rYXJyNGR2OW45In0.NQtYUieBSIfqm3LR5LrTsQ',
			maxZoom: 20,
			minZoom: 7,
			keyboard: true	})
		
		var osm2 = L.tileLayer('https://api.tiles.mapbox.com/v4/{id}/{z}/{x}/{y}.png?access_token={accessToken}', {
 	            attribution: 'Map data &copy; <a href="https://www.openstreetmap.org/">OpenStreetMap</a> contributors, <a href="https://creativecommons.org/licenses/by-sa/2.0/">CC-BY-SA</a>, Imagery © <a href="https://www.mapbox.com/">Mapbox</a>',
 	            id: 'mapbox.outdoors', accessToken: 'pk.eyJ1IjoianJnbW5keiIsImEiOiJjazA3YnJta3UwMnRoM21rYXJyNGR2OW45In0.NQtYUieBSIfqm3LR5LrTsQ'	})
				
		var map = L.map('map',{
			center: [ 14.098405, -87.203916],
			zoom:7,
			layers: osm,
			zoomControl: false,
			fullscreenControl: {pseudoFullscreen: false, position: 'topleft'},
			maxBounds: [[ 16.223256, -82.436450],[ 12.097389,-90.532233]]});
		
		var viewCenter = new L.Control.ViewCenter(map);
			map.addControl(viewCenter);
		
		var marcador = L.marker([14.098405, -87.203916]);
			map.addLayer(marcador)		
			marcador.bindPopup("Estadio Nacional Tiburcio Carias Andino");
			
		var marcador = L.marker([ 15.470019, -88.006789]);
			map.addLayer(marcador)		
			marcador.bindPopup("Estadio Olimpico Sampedrano");

		var marcador = L.marker([ 15.507453, -88.033430]);
			map.addLayer(marcador)		
			marcador.bindPopup("Estadio General Francisco Morazan");

		var marcador = L.marker([15.49537, -87.999058]);
			map.addLayer(marcador)		
			marcador.bindPopup("Estadio Yankel Rosenthal");

		var marcador = L.marker([15.78658, -86.785943]);
			map.addLayer(marcador)		
			marcador.bindPopup("Estadio municipal Ceibeño");

		var marcador = L.marker([13.295558, -87.149043]);
			map.addLayer(marcador)		
			marcador.bindPopup("Estadio Emilio Williams Agasse");	
			
		var marcador = L.marker([14.031904, -86.573226]);
			map.addLayer(marcador)
			marcador.bindPopup("Estadio Marcelo Tinoco");
			
		var marcador = L.marker([14.453589, -87.656791]);
			map.addLayer(marcador)
			marcador.bindPopup("Estadio Carlos Miranda Canales");
			
		var marcador = L.marker([14.658512, -86.216909]);
			map.addLayer(marcador)
			marcador.bindPopup("Estadio Juan Ramón Brevé Vargas");
		
		var miniMap = new L.Control.MiniMap(osm2,{ toggleDisplay: true, position: 'bottomright' }).addTo(map);
		
		var MousePosition = new L.control.mousePosition(osm).addTo(map);
		
		var escala = L.control.scale().addTo(map);		
		
		new L.Control.Zoom({ position: 'topright'}).addTo(map);
				
	</script>
		
    </body>
</html>	
	
