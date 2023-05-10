// This file contains commands and parameters to run the ctakes-examples "Hello World" pipeline <br/>
// with Entity Property output <br/>
 <br/>
// Load a simple token processing pipeline from another file <br/>
$\textcolor{orange}{\textsf{load}}$ [org/apache/ctakes/examples/pipeline/HelloWorld.piper](https://github.com/apache/ctakes/wiki/org/apache/ctakes/examples/pipeline/HelloWorld.piper) <br/>
 <br/>
// Assertion engines require dependencies <br/>
addDescription ClearNLPDependencyParserAE <br/>
// Add the Semantic Role Labeler parser for use by assertion <br/>
add ClearNLPSemanticRoleLabelerAE <br/>
 <br/>
// Use the assertion mini pipeline <br/>
// $\textcolor{orange}{\textsf{load}}$ [parameters](https://github.com/apache/ctakes/wiki/parameters) used by the following engines <br/>
$\textcolor{orange}{\textsf{load}}$ [org/apache/ctakes/examples/pipeline/AssertionDefaults.piper](https://github.com/apache/ctakes/wiki/org/apache/ctakes/examples/pipeline/AssertionDefaults.piper) <br/>
// the engines ... <br/>
add medfacts.AssertionAnalysisEngine <br/>
add medfacts.ConceptConverterAnalysisEngine <br/>
add attributes.SubjectAttributeAnalysisEngine <br/>
add attributes.GenericAttributeAnalysisEngine <br/>
 <br/>
// Collect discovered Entity information for post-run access <br/>
collectEntities <br/>
