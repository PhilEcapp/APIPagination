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
<h1 dir="auto">File 01 - index.html</h1>
