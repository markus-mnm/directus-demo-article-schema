# Directus demo schema

Requires JDK11+

And set api and token via environment variables:

    export DIRECTUS_ADMIN_TOKEN=some-uuid-set-as-token-for-an-admin ; export DIRECTUS_API_HOST=http://localhost:7000

This demo schema is both an example on how a schema could be managed as well as having a reference schema for bug reports.  

    demo_articles 
       demo_authors  - 1 author to many articles
       demo_article_translations - text in the main article that is available in different languages
       demo_sections - a section belongs to one articles, each article can have many sections)
       demo_articles_sections_translations - text a section that is available in different languages
       demo_layout - each section has a layout
    
    demo_content_languages


To apply the schema plus data run 

    # from the project root run
    ./gradlew --info drop-demo-collections
    ./gradlew --info apply-demo-collections


This project depends on https://github.com/markus-mnm/directus7javatools.git via a Gradle sourceControl dependency. See settings.gradle for the set up
For the first run it will download a number of dependencies, the total run time for the tasks should be < 30 seconds, thought that also depends on the speed of Directus



