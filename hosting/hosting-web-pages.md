# Hosting web pages

Web pages written in HTML, CSS, and JavaScript can be hosted on Replit. HTML/CSS/JS repls are given a unique URL that can be shared with your friends, family, peers, and clients.

After running a repl, your repl will be hosted at the URL provided in the `result` tab.

## URL Format

The repl will be hosted with the following URLs:
* `https://REPL-NAME--USERNAME.repl.co`
* `http://REPL-NAME.USERNAME.repl.co`

Where `REPL-NAME` is the name of the repl and `USERNAME` is the owner's username.

If you create a repl with a title that matches your username (i.e. repl.it/@username/username), it will be hosted at:
* `https://USERNAME.repl.co`


If an anonymous repl is created, the username used in the URL will be `five-nine`.

Note that if your username contains underscores `_`, they will be converted to dashes in the URL.

## Updating Websites

Changes made to your repl will not be reflected in the live version until the web project is re-run. Running a web repl will update its live version.

Note that a repl's public link will persist, even after the repl has been deleted. You can clear a repl of its server code before deleting it in order to prevent it from loading.

## Custom Domains

Any hosted repl can be linked to a domain that you own. This includes both [static sites](#hosting-a-web-site) and [HTTP servers](/repls/http-servers). To get started, you'll need a domain to link with your repl. If you don't already have a domain, [Dotcomboom](https://replit.com/@dotcomboom) has created a [great tutorial on getting a free domain from Freenom](https://replit.com/talk/learn/How-to-use-a-custom-domain/8834).

Once you have your domain link, we can get to work linking it with your repl: 

1. Click on the pencil icon next to the URL for your repl:

![screenshot of edit button](/images/repls/edit-custom-domain-icon.png)

2. Enter the full domain where you'd like the repl to be accessible from. This includes subdomains.

![screenshot of cname instructions](/images/repls/custom-domain-cname.png)

3. You will be prompted to add a `CNAME` record to your domain, pointing at your repl's special `repl.co` domain. 
4. Go to your domain registrar and find the section that allows you to add DNS records.
5. Add a new entry with the following information:
> * The type should be `CNAME`.
>* `name` or `hostname` will be the subdomain you want, or you can enter `@` if you'd like to use the full domain. Some services do not allow `CNAME`s to be at the top level. We recommend instead using _www_ and making sure you enter `www.yourdomain.com` in your repl.
>* `data` or `target` should be the special repl.co link you got when you started linking your repl. It should contain a long string of random numbers and letters at the beginning.

For example:
- If I want to serve a repl from `example.com`, I'd enter `example.com` in the repl linking box. Then, in my registrar the target should be `@`.
- If I want to serve a repl from `coolproject.example.com`, I'd enter `coolproject.example.com` in the repl linking box, and `coolproject` in the target field on my registrar.

The exact steps will vary between services. Here's an example of how it might look using Google Domains:

![screenshot of cname instructions](/images/repls/google-setup-custom-domain.png)

![screenshot of Cloudflare cname instructions](/images/repls/cloudflare-setup-custom-domain.png)

It may take some time for the DNS record to be updated. Once connected, click the big green button to finish and your domain should be linked!

You can unlink your domain at any time by clicking on the pencil icon and clicking "Unlink".

## Example

Here's an example of a hosted webpage using p5.js. The live, full-screen version can be found [here](https://p5-demo--timmy_i_chen.repl.co).

<iframe height="800px" width="100%" src="https://replit.com/@timmy_i_chen/p5-demo?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe>

## Takedown Requests

If you require your hosted web page to be taken down, please contact
us at [contact@replit.com](mailto:contact@replit.com).
