classFiles =  CompareCount.class Dictionary.class FileParser.class \
			SpellCheckUser.class TestList.class

spellchecker.jar : $(classFiles)
	jar cfe spellchecker.jar SpellCheckUser $(classFiles) && rm $(classFiles) && java -jar spellchecker.jar
CompareCount.class : CompareCount.java gitTasks
	javac CompareCount.java
Dictionary.class : Dictionary.java CompareCount.java TestList.java gitTasks
	javac Dictionary.java
FileParser.class : FileParser.java gitTasks
	javac FileParser.java
SpellCheckUser.class : SpellCheckUser.java gitTasks
	javac SpellCheckUser.java
TestList.class : TestList.java gitTasks
	javac TestList.java
.PHONY: gitTasks
gitTasks :
	git pull origin
.PHONY: clean
clean :
	rm spellchecker.jar $(classFiles)
