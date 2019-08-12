node("master"){
	print "Pipeline started"
def repoName = "CSharpHW"
dir("${WORKSPACE}\\${repoName}"){
 	def solutionFile = "${WORKSPACE}\\CSharpHW\\CSharpHW.sln"
	print "solutionFile : ${solutionFile}"
	def buildCmd = "MSBuild \"${solutionFile}\""
		print "Starting build"
	retCode =  bat (script: "$buildCmd", returnStatus: true);
	if(retCode != 0){
		error("Build Failed");
	}
	else{
		print 'Build Success'
	}
}
	print "Pipeline completed"
}