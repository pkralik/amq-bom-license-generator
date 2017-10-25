# amq-bom-license-generator
Maven project to generate licenses from AMQ BOM file

src/license
  licenses.xml	template XML containing complete list of product dependencies 
		(without versions)
  licenses.xsl	XSLT transformation for creating licenses.html
  licenses.css	CSS file to accompany licenses.html

pom.xml		imports BOM for versions
		passes <product> and <version> to XSLT transformation

Requires JDK 8 to build

Example build
  mvn clean package -Dmaven.repo.local=$HOME/m2-mead-amq7
