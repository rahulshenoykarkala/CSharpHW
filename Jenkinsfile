node("Test"){
print "Hello World"
def WORKSPACE = "C:\\Users\\rshenoy156537\\Desktop\\Techs\\jenkins"
def repoName = "CSharpHW"
print "WS: ${WORKSPACE}"
dir("${WORKSPACE}\\${repoName}"){
 	def solutionFile = "${WORKSPACE}\\CSharpHW\\CSharpHW.sln"
	print "solutionFile : ${solutionFile}"
	def buildCmd = "MSBuild ${solutionFile}"
	retCode =  bat (script: "$buildCmd", returnStatus: true);
	if(retCode != 0){
		error("build failed");
	}
	else{
		print 'SUCCESSFUL'
	}
}
}