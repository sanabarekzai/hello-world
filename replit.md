# Running the project

This is a static HTML project. Start the Replit web workflow to serve the main
`myfirstweb` page on port 5000:

```bash
python3 -c 'import http.server; Base=http.server.SimpleHTTPRequestHandler; Handler=type("Handler",(Base,),{"do_GET":lambda self: (setattr(self,"path","/myfirstweb"), Base.do_GET(self))[1] if self.path.split("?",1)[0]=="/" else Base.do_GET(self)}); Handler.extensions_map[""]="text/html"; http.server.ThreadingHTTPServer(("0.0.0.0",5000),Handler).serve_forever()'
```

The main `myfirstweb` HTML page is served at `/` and can also be opened directly
at `/myfirstweb`.