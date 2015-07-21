# 1.0.2 #

Updated some type hinting and **this.secure** now defaults to true if the page is loaded via HTTPS, false otherwise. 
Also fixed a small bug that would not allow cookies to be set on localhost (most likely due to it being a not 
entirely valid domain)
