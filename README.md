# Pdfjs::Rails

This gem wraps [Mozilla PDF.js](https://mozilla.github.io/pdf.js/) library
to display PDF in Rails apps inside the browser using pure Javascript.

## Installation

Add this line to your application's Gemfile:

    gem 'pdfjs-rails'

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install pdfjs-rails

## Usage

You can either include pdfjs in all your views by adding the following to your application.js and application.css:

    # application.js
    ...
    //= require pdfjs-rails
    ...

    # application.css
    ...
    *= require pdfjs-rails
    ...

or in specific views:

    # myview.html.erb
    ...
    <%= javascript_include_tag "pdfjs-rails" %>
    <%= stylesheet_link_tag "pdfjs-rails" %>

In the view you want to show the pdf viewer:

    ...
    <script> PDFJS.workerSrc = '<%= asset_path "pdf.worker"%>' </script>
    ...
    <%= pdf_viewer('PDF_URL_HERE') %>

## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Added some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request
