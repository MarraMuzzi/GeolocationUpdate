# GeolocationUpdate
Update to trying to set a geolocation to our prooject
<html>
<body>

<p>Click the button to get your coordinates.</p>

<button onclick="getgeoLocation()">Current location</button>

<p id="location"></p>

<script>
var m = document.getElementById("location");

function getgeoLocation() {
    if (navigator.geolocation) {
        navigator.geolocation.getCurrentPosition(showPosition);
    } else { 
        m.innerHTML = "No position found please try again.";
    }
}

function showPosition(position) {
    m.innerHTML = "Latitude: " + position.coords.latitude + 
    "<br>Longitude: " + position.coords.longitude;
}
</script>

</body>
</html>
