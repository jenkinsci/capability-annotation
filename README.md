Capability annotation should be used by plugins to declare it's capability
 
Example:
 
    pacakge io.jenkins.example.test;
    @Capability("io.jenkins.example.test.ExampleTestReporter")
    public class MyTestReporterAction extends AbstractTestResultAction {
        ...
    }

BlueOcean API would report this capability when queried using it's classes API as:

    GET /rest/classes/io.jenkins.example.test.MyTestReporter
    
    {
        "classes":["io.jenkins.example.test.ExampleTestReporter", "hudson.tasks.test.AbstractTestResultAction"]
    }
 