**Cartographic Spatial Extent (Bounding Box Coordinates)**

Linked Data for Libraries Cartographic Materials Working Group

Ontology Modeling Examples -- **Draft Version 2**, May 2018

**Ontologies**

@prefix bib:  <http://bibliotek-o.org/1.1/ontology/> .

@prefix bf:   <http://id.loc.gov/ontologies/bibframe/> .

@prefix gcro: <http://http://ontology.library.harvard.edu/geo/> .

@prefix geo:  <http://www.opengis.net/ont/geosparql#> .

@prefix rdau: <http://rdaregistry.info/Elements/u/> .

**Classes**

geo:Geometry

gcro:CartSource

**Object Properties**

	

	bib:hasSource

**Data Properties**

	geo:asWKT

	rdau:P60109 ["has coordinates of cartographic content“]

**Named Individuals of gcro:CartSource**

Sources for coordinate data	{based on MARC 034 $$2 Cartographic Data Source Code list 	[https://www.loc.gov/standards/sourcelist/cartographic-data.html](https://www.loc.gov/standards/sourcelist/cartographic-data.html)}:

	gcro:Bound		Bounding Box (Klokan Technologies)

	gcro:GeoNames	GeoNames.org

gcro:GNS		NGA GEOnet Names Server (GNS) 

gcro:GettyTGN	Getty Thesaurus of Geographic Names Online

gcro:GNIS		Geographic Names Information System (GNIS)

gcro:GooEarth		Google Earth

gcro:Wikiped		Wikipedia

**Illustration**

![image alt text](image_0.png)

-----

**Examples**

**	***Example 1*** - **Map of Australia, source of coordinates the Klokan Bounding Box Tool

		E 72°14'00"--E 168°13'00"/S 9°05'00"--S 55°19'00"

		:work1 rdau:P60109 :geometry1 .

		:geometry1 a geo:Geometry ;

			bib:hasSource gcro:Bound ;

geo:asWKT "POLYGON((72.2 -9.1, 168.2 -9.1, 168.2 -55.3, 72.2 -55.3, 	72.2 -9.1))"^^geo:wktLiteral .

	*Example 2*** - **Map of Prague, source of coordinates the map itself

		E 14°18'45"--E 14°29'15"/N 50°08'00"--N 50°01'30"

		:work2 rdau:P60109 :geometry2 .

		:geometry2 a geo:Geometry ;

			bib:hasSource :work2 ;

geo:asWKT "POLYGON((14.3125 50.13333, 14.4875 50.13333, 14.4875 		50.025, 14.3125 50.025, 14.3125 50.13333))"^^geo:wktLiteral .

		

	

