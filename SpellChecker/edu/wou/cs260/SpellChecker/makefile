spellchecker.jar : CompareCount.class Dictionary.class FileParser.class \
			SpellCheckUser.class TestList.class
	jar cfe spellchecker.jar SpellCheckUser CompareCount.class \
Dictionary.class FileParser.class SpellCheckUser.class TestList.class

CompareCount.class : CompareCount.java
	javac CompareCount.java
Dictionary.class : Dictionary.java CompareCount.java TestList.java
	javac Dictionary.java
FileParser.class : FileParser.java
	javac FileParser.java
SpellCheckUser.class : SpellCheckUser.java
	javac SpellCheckUser.java
TestList.class : TestList.java
	javac TestList.java
clean :
	rm spellchecker.jar CompareCount.class Dictionary.class \
FileParser.class SpellCheckUser.class TestList.class
