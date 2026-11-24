**Exploit (0 -> 1):** Information disclosure in page source. Password is an HTML comment the browser does not render. View the page source _(Cmd+U, Ctrl+U)_.

**Flaw:** Secrets left in client-side source. Anything the browser 
receives, the user can read.

**Tooling:** view page source
