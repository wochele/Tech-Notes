# Settings for VS Code

- [User and Workspace Settings](https://code.visualstudio.com/docs/customization/userandworkspace)

```
{
    "terminal.integrated.shell.windows": "\\windows\\system32\\WindowsPowerShell\\v1.0\\powershell.exe",
    "http.proxy": "http://mi%5C61408%3AAinjane24@PROXY_NAME:8080",
    "https.proxy": "http://mi%5C61408%3AAinjane24@PROXY_NAME:8080",
    "http.proxyStrictSSL": false
}
```

#### [From Working in Visual Studio behind the Firewall](https://taeguk.co.uk/blog/working-in-visual-studio-behind-the-firewall/)

Visual Studio Code is a tricky one to setup because it isn’t .NET, it’s all JavaScript based. Most of my information came from the GitHub issue.

- Determine your proxy server and port. When you have a complicated proxy, this is a pain and it took me a while as I use an automatic configuration script. If it is a standard server/port combo, you’re on an easier path.
- I usually configure IE with a script from a URL like this one: http://proxy-server/script.dat. This is a plain JS script which, after a bit of looking at, I discovered pointed to proxy-cluster.fqdn.local:8881.
- Now I have a server and port I need my authentication details. The format for these is DOMAIN\User Name:P@ssword! but has to be URL encoded. A simple online URL encoded translated that into: DOMAIN%5CUser%20Name%3AP%40ssword!
- Piece all this info into a single string like so: http://DOMAIN%5CUser%20Name%3AP%40ssword!@proxy-cluster.fqdn.local:8881
- Then add this into your User Settings in File, Preferences against the "http.proxy" value:
- [URL Encoder](http://meyerweb.com/eric/tools/dencoder/)

```
// Place your settings in this file to overwrite the default settings
{
    "http.proxy": "http://DOMAIN%5CUser%20Name%3AP%40ssword!@proxy-cluster.fqdn.local:8881"
}
```

There are a lot of ways to mess this up, I almost gave up on VS Code after weeks of messing about, the removal of C# from base product made it “make or break time”. If you are struggling I suggest you re-read the GitHub issue. The main tip I found useful was to pop-open the Developer Tools in VS Code (under Help) and in the JavaScript Console run: require('url').parse('YOUR PROXY URL') and check the output.
