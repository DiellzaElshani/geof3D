```
@prefix geof3d: <https://w3id.org/geof3d#> .
@prefix dct:   <http://purl.org/dc/terms/> .
@prefix owl:   <http://www.w3.org/2002/07/owl#> .
@prefix rdf:   <http://www.w3.org/1999/02/22-rdf-syntax-ns#> .
@prefix rdfs:  <http://www.w3.org/2000/01/rdf-schema#> .
@prefix xsd:   <http://www.w3.org/2001/XMLSchema#> .

#################################################################
# Ontology header
#################################################################

geof3d: a owl:Ontology ;
    dct:title "geof3D Vocabulary: SPARQL Geometric Functions for 3D Geometry"@en ;
    dct:creator "Diellza Elshani" ;
    dct:publisher <https://w3id.org/geof3d#> ;
    dct:license <https://creativecommons.org/licenses/by/4.0/> ;
    rdfs:comment """
The geof3D vocabulary defines IRIs for SPARQL built-in functions supporting
3D geometric computation in RDF-based workflows. The vocabulary is conceptual
and independent of any specific software implementation.
"""@en ;
    owl:versionInfo "0.1.0" .

#################################################################
# Core class
#################################################################

geof3d:GeometricFunction a owl:Class ;
    rdfs:label "Geometric function"@en ;
    rdfs:comment "A conceptual geof3D SPARQL built-in function."@en .

#################################################################
# Measurement & analysis functions
#################################################################

geof3d:distance3D a geof3d:GeometricFunction ;
    rdfs:label "distance3D"@en ;
    rdfs:comment "Computes the 3D distance between two geometries (G × G → R)."@en .

geof3d:area a geof3d:GeometricFunction ;
    rdfs:label "area"@en ;
    rdfs:comment "Computes the area of a geometry, typically surface area (G → R)."@en .

geof3d:volume a geof3d:GeometricFunction ;
    rdfs:label "volume"@en ;
    rdfs:comment "Computes the volume of a closed solid geometry (G → R)."@en .

geof3d:centroid a geof3d:GeometricFunction ;
    rdfs:label "centroid"@en ;
    rdfs:comment "Computes the centroid of a geometry and returns a point geometry (G → G′)."@en .

#################################################################
# Relational / predicate functions
#################################################################

geof3d:within3D a geof3d:GeometricFunction ;
    rdfs:label "within3D"@en ;
    rdfs:comment "Tests whether geometry A is within geometry B in 3D (G × G → boolean)."@en .

geof3d:covers3D a geof3d:GeometricFunction ;
    rdfs:label "covers3D"@en ;
    rdfs:comment "Tests whether geometry A covers geometry B in 3D (G × G → boolean)."@en .

geof3d:intersectBoolean a geof3d:GeometricFunction ;
    rdfs:label "intersectBoolean"@en ;
    rdfs:comment "Boolean test for intersection between two geometries (G × G → boolean)."@en .

geof3d:unionBoolean a geof3d:GeometricFunction ;
    rdfs:label "unionBoolean"@en ;
    rdfs:comment "Boolean test related to union of two geometries (G × G → boolean)."@en .

geof3d:isValid a geof3d:GeometricFunction ;
    rdfs:label "isValid"@en ;
    rdfs:comment "Tests whether a geometry is valid according to geometric constraints (G → boolean)."@en .

#################################################################
# Constructive Boolean (geometry-returning) functions
#################################################################

geof3d:intersection3D a geof3d:GeometricFunction ;
    rdfs:label "intersection3D"@en ;
    rdfs:comment "Computes the 3D intersection of two geometries (G × G → G′)."@en .

geof3d:union3D a geof3d:GeometricFunction ;
    rdfs:label "union3D"@en ;
    rdfs:comment "Computes the 3D union of two geometries (G × G → G′)."@en .

geof3d:difference3D a geof3d:GeometricFunction ;
    rdfs:label "difference3D"@en ;
    rdfs:comment "Computes the 3D difference A \\ B (G × G → G′)."@en .

geof3d:symDifference3D a geof3d:GeometricFunction ;
    rdfs:label "symDifference3D"@en ;
    rdfs:comment "Computes the 3D symmetric difference (XOR) of two geometries (G × G → G′)."@en .

#################################################################
# Transformational / affine functions
#################################################################

geof3d:extrude a geof3d:GeometricFunction ;
    rdfs:label "extrude"@en ;
    rdfs:comment "Extrudes a geometry along a vector to create a solid (G × v → G′)."@en .

geof3d:translate a geof3d:GeometricFunction ;
    rdfs:label "translate"@en ;
    rdfs:comment "Translates a geometry by a vector offset (G × v → G′)."@en .

geof3d:rotate a geof3d:GeometricFunction ;
    rdfs:label "rotate"@en ;
    rdfs:comment "Rotates a geometry around an axis or angle (G × θ → G′)."@en .

geof3d:transform a geof3d:GeometricFunction ;
    rdfs:label "transform"@en ;
    rdfs:comment "Applies an affine transformation matrix to a geometry (G × M → G′)."@en .

geof3d:negate a geof3d:GeometricFunction ;
    rdfs:label "negate"@en ;
    rdfs:comment "Negates geometry coordinates or vector components (G → G′)."@en .
```
