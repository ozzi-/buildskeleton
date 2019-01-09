This is a very basic skeleton for building fat JARs (runnable and containing all maven depednencies) through Jenkins 
and pushing the JAR to Artifactory (Universal Artifact Repository Manager).

The generated JAR in Artifactory will contain the build number of Jenkins in the filename. 

Check the XML files for comments describing the single values.

The following two screenshots show the basic configuration needed for the Jenkins build job.

![sourcecode management settings in jenkins](https://raw.githubusercontent.com/ozzi-/buildskeleton/master/sc_mgmt_jenkins.png)

![build settings in jenkins](https://raw.githubusercontent.com/ozzi-/buildskeleton/master/build_settings_jenkins.png)
