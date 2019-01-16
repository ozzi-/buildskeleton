# What?

This is a very basic skeleton for building fat JARs (runnable and containing all maven depednencies) through Jenkins 
and pushing the JAR to Artifactory (Universal Artifact Repository Manager).

The generated JAR in Artifactory will contain the build number of Jenkins in the filename. 

Check the XML files for comments describing the single values.

The following two screenshots show the basic configuration needed for the Jenkins build job.

![sourcecode management settings in jenkins](https://raw.githubusercontent.com/ozzi-/buildskeleton/master/sc_mgmt_jenkins.png)

![build settings in jenkins](https://raw.githubusercontent.com/ozzi-/buildskeleton/master/build_settings_jenkins.png)

## Make your program aware of the build number

If you want to make your fat jar aware of the build number too, do the following:

1. Create a variable to hold the build number
![java variable](https://raw.githubusercontent.com/ozzi-/buildskeleton/master/inject_into_variable_into_code_1.png)

2. Install content replace (https://wiki.jenkins.io/display/JENKINS/Content+Replace+Plugin) on your jenkins

3. Add a pre step content replace searching for (REPLACED_BY_JENKINS) and replacing with ${BUILD_NUMBER}
![jekins pre step](https://raw.githubusercontent.com/ozzi-/buildskeleton/master/inject_into_variable_into_code_2.png)

This will lead to the java variable buildID holding the value of BUILD_NUMBER.
