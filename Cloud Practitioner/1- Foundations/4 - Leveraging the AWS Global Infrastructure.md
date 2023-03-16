# Regions

A Region is a physical location.
 - US West
 - US East
	 - Ohio
	 - N. Virginia
 - South America
 - Europe
 - Africa
 - Asia Pacific

 AWS logically groups its Regions into geographic locations.

This allows fast loading and lower [[#Latency]] for user base don geo-location

## Region Characteristics

Fully independent and isolated
 - if one region is impacted, the others will not be

Resource and service specific
 - Regions are isolated, and resources aren't automatically replicated across them
___

# Availability Zones or AZ

Availability Zones consist of one or more physically separated data centers,
each with redundant power, networking, and connectivity, housed in separate facilities.

## Characteristics of AZs

AZ are connect among themselves in a single region
 - Physically separated
 - Connected through low-latency links
 - Fault tolerant
 - Allows for high availability
___

# Edge Locations

 - more then there are AZ's
 - Edge locations cache content for fast delivery to your users.
 - Mini data center
 - **Distribution Cache** is the Name given to the collection of edge locations

# Term

##### Latency

>Latency is the time that passes between a user request and the resulting response.
>
> lower is better