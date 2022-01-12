<h2 dir="auto">API Pagination</h2>

JSON:API allows four types of pagination links: prev , next , first , and last . It is RECOMMENDED that servers include first and last links when these are inexpensive to compute. However, servers MUST include a prev and a next link for each instance of paginated data in a response.

    PART 01: JSON Code/ Http/s URL
    PART 02: Fetch JSON data
    PART 03: Display in/on HTML
    PART 04: Attached Links/URL's needed
    
<h2 dir="auto">JSON CODE/URL</h2>
This is the js to fetch data from JSON file. 
<pre>
var json = {
    "Product": [
        {
            "Key1": "Value1 A"
        },
        {
            "Key1": "Value1 B"
        },
        {
            "Key1": "Value1 C"
        },
        {
            "Key1": "Value1 D"
        },
        {
            "Key1": "Value1 E"
        },
        {
            "Key1": "Value1 F"
        },
        {
            "Key1": "Value1 G"
        },
        {
            "Key1": "Value1 H"
        },
        {
            "Key1": "Value1 I"
        }
    ]
}
</pre>

<h2 dir="auto">FETCH JSON DATA</h2>
This is the js to fetch data from JSON file.
<pre>
$('#list').pagination({ // you call the plugin
  dataSource: json.Product, // pass all the data
  pageSize: 2, // put how many items per page you want
  callback: function(data, pagination) {
      // data will be chunk of your data (json.Product) per page
      // that you need to display
      var wrapper = $('#list .wrapper').empty();
      $.each(data, function (i, f) {
         $('#list .wrapper').append('

    Key1: ' + f.Key1 + '

');
      });
    }
   });
</pre>

<h2 dir="auto">FETCH JSON DATA VIA URL</h2>
This is the js to fetch data from JSON URL.
<pre>
$.getJSON('data/people.json', function (json) {
    $('#list').pagination({
        dataSource: json.Product,
        pageSize: 2,
        callback: function(data, pagination) {
            var wrapper = $('#list .wrapper').empty();
            $.each(data, function (i, f) {
                $('#list .wrapper').append('

    Key1: ' + f.Key1 + '

');
            });
        }
    });
});
</pre>

<h2 dir="auto">DISPLAY IN HTML</h2>
This is HTML section where result displayed.
<pre>
<code>
<div id="list"><div class="wrapper"></div></div>
</code>
</pre>

<h2 dir="auto">INCLUDE LINKS/FILES</h2>
Scripts, JS and CSS files
<pre>
<script src="https://code.jquery.com/jquery-3.4.1.min.js"></script>
<script src="https://pagination.js.org/dist/2.1.4/pagination.min.js"></script>
<link rel="stylesheet" href="https://pagination.js.org/dist/2.1.4/pagination.css"/>
</pre>

![pag](https://user-images.githubusercontent.com/74012005/149208840-cbd93bb4-5789-476b-bcef-d43178449609.jpg)
