# Summernote Plugin elFinder
Summernote Plugin for elFinder File Manager

## Installation
- Download plugin files. Extract it and copy into your summernote plugin directory.
- Include the summernote ext javascript file into your html page.

    ```javascript
    <script src="path/to/plugin/summernote-ext-elfinder/summernote-ext-elfinder.js"></script>
    ```


- Initialize the plugin at your summernote initialization code.

    ```javascript
    <script type="text/javascript">
      $(function() {
        $('.summernote').summernote({
          height: 200,
          tabsize: 2,
          toolbar: [
              ['style', ['bold', 'italic', 'underline', 'clear']],
              ['insert', ['elfinder']]
            ]
        });
      });
      function elfinderDialog() {
      	var fm = $('<div/>').dialogelfinder({
      		url : 'https://path.to/your/connector.php', // change with the url of your connector
      		lang : 'en',
      		width : 840,
      		height: 450,
      		destroyOnClose : true,
      		getFileCallback : function(files, fm) {
      			console.log(files);
      			$('.editor').summernote('editor.insertImage', files.url);
      		},
      		commandsOptions : {
      			getfile : {
      			oncomplete : 'close',
      			folders : false
      			}
      		}
      	}).dialogelfinder('instance');
      }
    </script>
    ```

## Tested with
- Summernote : master branch (after v0.8.1)
- elFinder : 2.1.9
- Bootstrap : v3.3.6
- jQuery : 1.12.1
- jQuery-UI : 1.11.4

## NOTE :
Don't forget to include the jQuery and jQuery-UI. The latest elFinder not include jquery-ui file.
