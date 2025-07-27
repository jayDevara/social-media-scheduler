# Social Share Scheduler on LinkedIn with Django & Inngest

Automate and schedule social sharing on LinkedIn via Python, Django, & Ingest

Sharing posts on LinkedIn through Python and Django is a very easy process. Get some API keys and send an HTTP POST Request.

What's not so easy, is reliably scheduling those posts for a later date, especially with Django alone. Inngest is a huge unlock to do exactly this.

What's more, setting up a system that is ready to share not just on LinkedIn but any other social platform that has an API to do so.

So we need to solve two primary things:

- OAuth - Connecting LinkedIn users to our Django users
- Scheduling/Offloading tasks - Using just Django and Inngest, we'll run our tasks later


The OAuth process is this:

- We create an "App" on LinkedIn (or Facebook or X or Discord or whatever)
- We connect that "LinkedIn App" to our Python code via API Keys through Environment Variables
- Django & Django AllAuth are configured with those keys
- User logs in clicking the "Login with LinkedIn" button
- Django and LinkedIn talk to ensure all permissions are valid
- LinkedIn shares an Access Token to Django, Django stores it
- Through Django, our code can now post to LinkedIn via the LinkedIn API, our LinkedIn App, a User's Access Token, and an HTTP Request
