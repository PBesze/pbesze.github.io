---
title: "Implementing compareTo()"
excerpt: "implementing-compareTo"
sitemap: true
permalink: /sample-codes/implementing-compareTo/
author_profile: true
---
The compareTo() method is another way of comparing objects:

~~~~

	// TODO: Add the method:
	// public int compareTo(EarthquakeMarker marker)
  public int compareTo(EarthquakeMarker marker){
		if (marker.getMagnitude()>this.getMagnitude()){return 1;}
		if (marker.getMagnitude()<this.getMagnitude()) {return -1;}
		if(marker.getMagnitude()==this.getMagnitude()) {return 0;}
	return 0;
		}
    
 ~~~~
