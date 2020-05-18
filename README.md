How to read a properties from the standard application.properties with Spring Boot and @Value.<br/>
<br/>
How to compile and execute :<br/>
mvn package<br/>
java -jar ./target/waysToConfigureASpringApplication-0.0.1-SNAPSHOT.jar<br/>
<br/>
<br/>
---application.properties<br/>
myString=qwerty<br/>
---MyConfigurationBean.java<br/>
@Value("${myString}")<br/>
private String someConfigurationProperty;<br/>
---The class who displays the value of the 'myString' configuration<br/>
@Autowired<br/>
MyConfigurationBean myConf;<br/>
...<br/>
System.out.println(myConf.getSomeConfigurationProperty());<br/>
<br/>
<br/>
The application will read the value 'qwerty' of the property myString in the standard application.properties configuration file then display it in the terminal.<br/>


