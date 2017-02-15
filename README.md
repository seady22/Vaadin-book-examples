# Vaadin-book-examples
Some examples of the vaadin framework
1. Importing

You should create the server before importing, as the project files may refer to it as a compilation target. Not sure if it is relevant

    Create TomEE server in Eclipse
        In the Servers view, right-click → New → Server
        In the "New Server" wizard:
            Select Apache → Tomcat 7.0 Server
            Set Server name: "Apache TomEE 1.7 at localhost"
            Click Next
        In the Tomcat Servet step:
            Name: "Apache TomEE 1.7 at localhost"
            Installation Directory: "/opt/apache-tomee-webprofile-1.7.1"
            JRE: Workbench default or Java 8 JRE
            Click Finish

    Import project
        File → Import → Existing projects intro workspace
        In the import wizard:
            Select the cloned project directory
            Click Finish

2. Building

    Some Vaadin add-ons may require a snapshot version, which must be built and installed to the local Maven repository.

    For example, for Vaadin Charts:

    $ git clone https://github.com/vaadin/charts
    $ cd charts
    $ mvn install -DskipTests

    Refresh Ivy
        Right-click on project, select Ivy → Refresh

    Install license keys for commercial Vaadin add-ons (Charts, etc.)

    Compile the widget set
        Select Java Resources → src/com.vaadin.book.widgetset/BookExamplesWidgetSet.gwt.xml
        Click Compile Widgetset in the toolbar (requires Vaadin Plugin for Eclipse)

    You can also compile the themes here, or let them be compiled on-the-fly.

3. Deployment

Just add the project to the previously created TomEE server.

You should then be able to run the application with:

http://localhost:8080/book-examples-vaadin7/book

5. Development

Things you should notice:

    The examples are formatted by hand, so you must not have any automatic code formatting enabled in your Eclipse default settings.

6. Contributions

Contributions must go through the Gerrit code review system.

    You must install the commit-msg hook as instructed
    You must push to review as instructed
