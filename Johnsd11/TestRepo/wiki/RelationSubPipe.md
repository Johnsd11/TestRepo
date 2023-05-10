// Commands and parameters to create a default relation extraction sub-pipeline.  This is not a full pipeline. <br/>
 <br/>
// Modifiers. Use addLogged to log start and finish of processing.  There aren't default models, so set specifically <br/>
add ModifierExtractorAnnotator classifierJarPath=/org/apache/ctakes/relation/extractor/models/modifier_extractor/model.jar <br/>
 <br/>
// Degree of severity, etc. <br/>
add DegreeOfRelationExtractorAnnotator classifierJarPath=/org/apache/ctakes/relation/extractor/models/degree_of/model.jar <br/>
 <br/>
// Location. <br/>
add LocationOfRelationExtractorAnnotator classifierJarPath=/org/apache/ctakes/relation/extractor/models/location_of/model.jar <br/>
