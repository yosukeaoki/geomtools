# geomtools
Tools to convert Geocentric to WGS84 and WGS84 to UTM. 

## Prerequisite
numpy
pyproj

## Installation of prerequisites
% conda install -c conda-forge numpy pyproj 

## Running the test program
% python example.py

## gcs2llh
gcs2llh converts geocentric XYZ coordinates to WGS84 Latitude-Longitude-Height coordinate. 

    Usage: 
    llh = gcs2llh(xyz)
    
    Input: 
    xyz: Geocentric coordinates (N*3, where N is the number of sites, in meters) 
    
    Output: 
        llh: Longitude (Column 0), Latitude (Column 1), and height (Column 2, in meters)


## ll2UTM
ll2UTM converts Longitude-Latitude coordinates in WGS84 into the specified UTM coordinates. 

    Usage: 
    xy = ll2UTM(ll, EPSG)
    
    Input: 
        ll: Longitude (Column 0) and Latitude (Column 1) in degrees 
        EPSG: Coordinate system                 
            EPSG:32651  UTM51 (120-126E)
            EPSG:32652  UTM52 (126-132E)
            EPSG:32653  UTM53 (132-138E)
            EPSG:32654  UTM54 (138-144E)
            EPSG:32655  UTM55 (144-150E)
    Output:  
        xy: UTM coordinates in kilometers
