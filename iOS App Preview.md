# From the review doc

# Client

- [ ] hide the 'Buy more sessions' button from this route /client/calendar
	 
	 Status: Done ✅

	 Additionally i have hidden the similar button from this routes as well
		- /client/sessions/remaining
		- /purchases

- [ ] Move Pause and Close account to Account settings (main) page:
 	 
	 Status: already done (/client/settings/index). No need to change anything


- [ ] Guideline 3.1.1 (IAP) — reply, not StoreKit
	 Apple flagged digital products bought outside IAP. The review doc already has the reply: admin-only app, no checkout in iOS, commerce is on the web. 
	 Optional: audit leftover purchase UI so they don’t reject again.

# Coach
- [ ] Move Pause and Close account to Account settings (main) page:
 	Status: already done (/coach/settings). No need to change anything

- [ ] On the plans page, add a box at the bottom with buttons to Pause Account and Close account. These will redirect to the main settings page so people won’t get confused where it went.
	 Status: already done on the website. for iOS we have hidden the plans page. so, nothing to do.

- [ ] Fix Take Photo crash (iPad) (/coach/coaching-packages)
	 Coach flow: Offers → Packages → Create package → Select file → Take Photo → crash on iPad Air / iPadOS 18.6.2.\
	 DropzoneField already tries to block the camera on iOS; Apple still hit Take Photo.

	 Status: Done ✅
	 <mark> Note: Need to verify this from an iPad </mark>



# Leftover purchase UI that can still get an App Store rejection, grouped by risk.

- [ ] Purchases → session credits: Purchase (web only)
	 Disabled but still visible. Same pattern as the rejected Buy More button.
	 Route: /purchases
	 
	 Status: Done ✅

- [ ] Book appointment: Purchase More Sessions
	 Shows when that session type has 0 credits. No iOS hide.
	 Route: /client/sessions/create
	 
	 Status:

- [ ] Book appointment: Pay now
	 Shows when booking is blocked for unpaid sessions. Goes to checkout.
	 
	 Status: Done ✅\
	 Webview &darr;
	 
	 iOS View &darr;
	 

- [ ] Calendar / session list: Pay now
	PaymentStatusBadge opens checkout_url in a new tab.
	http://app.test/client/calendar
	 
	 Status: Done ✅\
	 Webview &darr;
	 <img width="2800" height="1800" alt="pay-now-web" src="https://github.com/user-attachments/assets/826df0ed-7dda-40b9-bd56-4bf1c3bbb1c6" />

	 iOS view &darr;
	 <img width="2800" height="1800" alt="pay-now-ios" src="https://github.com/user-attachments/assets/bb6bc587-1637-4581-8ba4-dc29a63ecfad" />


- [ ] Purchases → products: Re Subscribe
	Memberships with a checkout_url still link to checkout on iOS.
	 
	 Status: Done ✅\
	 Webview &darr;
	 <img width="2880" height="1800" alt="resubscribe-web" src="https://github.com/user-attachments/assets/2b11a5e0-8173-4286-920b-09eb0f1c9816" />

	 iOS view &darr;
	 <img width="2880" height="1800" alt="resubscribe-ios" src="https://github.com/user-attachments/assets/ca552d5f-3d17-436b-aba2-106d5dde8635" />


- [ ] Offer/product previews: Buy Now / CTA → /checkout/...
	Package, course, session, digital product, membership, and in-app package preview. Apple’s path was Offers → Packages; Preview still has a real checkout button.
	 
	 Status:

- [ ] Purchases footer: “Additional purchases are only available on your coach’s web platform.”
	 
	 Status:

- [ ] Coach’s Offerings (client store) footer: “browsing and purchasing are only available on the web platform…”
	Store grid is hidden, but this copy still talks about buying outside the app.
	 
	 Status:

- [ ] Purchases empty states: Browse Store
	Still shown on iOS and points at the store.
	 
	 Status:

## Coach side commerce

- [ ] LCH Store → Buy Now
	Coaches can buy LCH digital products in the app. Plans is hidden on iOS; this sidebar item is not.
	 
	 Status:

- [ ] My Store Link
	Public store URL plus “Clients will complete purchases outside the app.”
	 
	 Status:

- [ ] 
- [ ] 
- [ ] 
- [ ] 
