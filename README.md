# DocRaptor JS Demo

This is a simple demo intended to showcase DocRaptor's ability to parse JavaScript before the PDF export is generated.

## Instructions

To generate a PDF, open up your computer's terminal. Enter the following cURL command to initiate an HTTP request:

### With JavaScript Executed

```sh
curl http://YOUR_API_KEY_HERE@docraptor.com/docs \
  --fail --silent --show-error \
  --header "Content-Type:application/json" \
  --data '{"test": true,
           "javascript": true,
           "document_url": "http://tylerhawkins.info/docraptor-js-demo/",
           "type": "pdf" }' > docraptor_js_demo.pdf
```

### Without JavaScript Executed

```sh
curl http://YOUR_API_KEY_HERE@docraptor.com/docs \
  --fail --silent --show-error \
  --header "Content-Type:application/json" \
  --data '{"test": true,
           "document_url": "http://tylerhawkins.info/docraptor-js-demo/",
           "type": "pdf" }' > docraptor_js_demo.pdf
```

You should now have a PDF document in the same directory from which you ran the above command.
