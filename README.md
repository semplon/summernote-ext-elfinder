# Summernote Plugin elFinder
Summernote Plugin for elFinder File Manager

## Installation
- Download plugin files. Extract it and copy into your summernote plugin directory.
- Include the summernote ext javascript file into your html page.

    ```javascript
    <script src="path/to/plugin/summernote-ext-elfinder/summernote-ext-elfinder.js"></script>
    ```

- Change the Value of the URL at the elFinder Callback file. Replace it with your elfinder connector url.
- Include the summernote callback javascript into your html page.

    ```javascript
    <script src="path/to/plugin/summernote-ext-elfinder/elfinder-callback.js"></script>
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
