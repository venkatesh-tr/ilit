## NGINX - URI/URL too large issue

Because NGINX or any other HTTP server like Apache has a limit for the requested URL for a resource. This limit is usually 8K in nginx. If the URL has more than this limit, it throws error "URL Too Large" (**414** response code). 

To fix this issue, set the following parameters inside the **sites-available/default** or the configuration file that your server uses.

`
Syntax:	large_client_header_buffers number size;
Default:	
large_client_header_buffers 4 8k;
Context:	http, server
`

I changed it to `large_client_header_buffers 8 16k;` to fix my server once.

