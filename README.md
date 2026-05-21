# paynow.sankhacooray.com

Experimental sandbox for tap-testing which Singapore payment-app deep-link
schemes actually open on a given phone. Lists DBS PayLah!, DBS digibank,
OCBC Digital, OCBC Pay Anyone, UOB TMRW, UOB Mighty, GrabPay, Singtel Dash,
ShopeePay, plus generic `tel:` / `sms:` sanity checks.

The page lets you edit the recipient (mobile / UEN / NRIC), amount, and
reference, then tap each variant to see which combination of `scheme://path`
actually launches the app on iOS or Android.

## Run locally

```
python3 -m http.server 8000
# open http://localhost:8000
```

Custom URL schemes will not resolve on desktop — open on a phone with the
relevant app installed.

## Deploy

Pushed to `main` on https://github.com/sankhacooray/paynow-sankhacooray-com
and served by GitHub Pages with the CNAME `paynow.sankhacooray.com`
(DNS via Cloudflare on the `sankhacooray.com` zone).

## Add a scheme

Edit `SCHEMES` in `index.html` — each row is `{app, variant, scheme}`.
`{mobile}`, `{amount}`, `{ref}` are substituted from the form fields.
