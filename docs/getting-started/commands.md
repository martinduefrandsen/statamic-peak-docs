# Commands

Peak comes with a set of CLI commands to make tedious recurring tasks a lot easier.

## Add Collection
This command creates a new collection and scaffolds out all needed files with some sane default markup containing the various Peak utilities we use.

Run `php please peak:add-collection` to:

* Create a collection in `content/collections/{handle}.yaml` with the variables you defined in the CLI.
* Create a blueprint for collection in `resources/blueprints/collections/pages/{handle}.yaml` containing the page builder fieldset and the SEO tab when your collection has a public route defined.
* Optionally create an index partial in `resources/views/{handle}/index.antlers.html` with default Peak markup.
* Optionally set the index template to the entry you chose to mount the collection on.
* Optionally create a show partial in `resources/views/{handle}/show.antlers.html` with default Peak markup.
* Optionally add permissions to the `editor` role in `resources/users/roles.yaml`.

## Add Page Builder Block
This command adds a block to the Peak Page Builder and generates the files needed.

Run `php please peak:add-block` to:

* Pick a group to add the block to.
* Add a set to the Page Builder replicator in `resources/fieldsets/page_builder.yaml`.
* Create a fieldset for your block in `resources/fieldsets/{file_name}.yaml`.
* Create a partial with default markup and IDE hinting in `resources/views/page_builder/_{file_name}.antlers.html`.

## Add Page Builder Article Set
This command adds a set to the Peak Page Builder Article (Bard) block and generates the files needed.

Run `php please peak:add-set` to:

* Pick a group to add the set to.
* Add a set to the Article Bard in `resources/fieldsets/article.yaml`.
* Create a fieldset for your set in `resources/fieldsets/{file_name}.yaml`.
* Create a component partial with default markup and IDE hinting in `resources/views/components/_{file_name}.antlers.html`.

## Add Partial
With this command you can choose a type (component, layout, snippet or typography) and add a name and description. It will generate a partial with the proper IDE hinting and location comments.

Run `php please peak:add-partial`.

## Clear site
This command clears the default Peak content.

Run `php please peak:clear-site` to:

* Delete all assets from the default asset container.
* Delete all entries but `home`.
* Clear the pagebuilder for the homepage.
* Clear the social media globals.
* Clear caches.

## Install Page Builder Block
This command installs premade blocks to the Peak Page Builder and generates the files needed.

Run `php please peak:install-block` to pick a block and:

* Add a set to the Page Builder replicator in `resources/fieldsets/page_builder.yaml`.
* Create a fieldset for the installed block in `resources/fieldsets/{file_name}.yaml`.
* Create a partial with bespoke markup in `resources/views/page_builder/_{file_name}.antlers.html`.

These are the page builder blocks available:
* **Call to action**: Show a call to action.
* **Collection**: Show collection entries.
* **Columns**: Text columns with optional images and buttons.
* **Divider**: A visual divider between blocks.
* **Full width image**: A full width image with optional text and button(s).[full_width_image]
* **Index content**: Render the currently mounted entries if available.
* **Image and text**: An image and text side by side.
* **Images grid**: A multi row image grid.
* **Link blocks**: Blocks that link using the button fieldset.
* **Text columns**: Text wrapping in two columns.

## Install Preset
This command installs full presets into Peak. A preset can be anything. A collection that installs the relevant blueprints, templates, configuration, pages and page builder blocks into your site or a simple navigation pattern or dark mode.

Run `php please peak:install-preset` to pick a set.

These are the presets available:
* **Breadcrumbs**: A breadcrumbs partial using schema markup.
* **Business hours**: A business hours global and a list and call component that shows the business hours and if the business is currently open / available.
* **Clients**: A routeless renamable client/partner collection with a logo cloud page builder block.
* **Events**: A dated events collection with index and show templates (including JSON-ld) and a page builder set.
* **FAQ**: A FAQ collection with a page builder set (including JSON-ld).
* **Language picker**: A language picker for when you use multisite.
* **Modal**: A modal that only has to be rendered once but can be used multiple times with different content.
* **News**: A dated news collection with index and show templates (including JSON-ld) and a page builder set.
* **Search**: A search form component and a styled search results template.
* **Theme toggle**: A theme toggle typically used for a Tailwind class based dark mode.
* **Vacancies**: A dated renamable vacancies collection with index and show templates (including JSON-ld).
