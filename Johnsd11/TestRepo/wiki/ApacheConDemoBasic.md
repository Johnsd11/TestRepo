 <br/>
// Run using command line parameters <br/>
// -p ApacheConDemoBasic <br/>
// -i org/apache/ctakes/examples/notes/apache_con/Patient123 <br/>
// -o {your output directory} <br/>
 <br/>
// Use our simple extension of AbstractFileTreeReader. <br/>
reader ApacheConDemoReader <br/>
 <br/>
// Add our simple regex engine to the pipeline. <br/>
// By default finds "biopsy". <br/>
add ApacheConDemoEngine <br/>
 <br/>
// Add our simple regex engine to the pipeline. <br/>
// Find Imaging mentions. <br/>
add ApacheConDemoEngine REGEX_CUI=AC456 REGEX="diagnostic imaging|MRI" <br/>
 <br/>
// Use our simple extension of AbstractJCasFileWriter. <br/>
add ApacheConDemoWriter <br/>
 <br/>
add FileTreeXmiWriter SubDirectory=XMI <br/>
