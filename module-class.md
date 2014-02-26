# Module Class

The module class is responsible for loading module specific configuration, including:

 - Plugins
 - Routes
 - Settings

Most of this is handled automatically by extending `Mammoth\Module` or `Mammoth\Application`

# Application Class

Typically there is one Application class in a project. This class loads all other modules, dispatches the routes, then handles responses. 

## Loading plugins

Some modules can be plugged into. When available they will call a `configureExamplePlugins` method on the application and all loaded modules. The typical call-ins are showing below:

    namespace MammothExample;
    use XMod\Module\Application;
    
    class System extends Application {

        ...
    
	    public function configureCMSPagePlugins($registry) {
			$registry->add(new ExamplePlugin());
	    }
	    
	    public function configureFormBuilderFormPlugins($registry) { ... }
	    public function configureFormBuilderSubmissionPlugins($registry) { ... }
	    public function configureArticlePlugins($registry) { ... }
	    public function configureSectionPlugins($registry) { ... }
    
    } 