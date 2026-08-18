# From the review doc

# Client

- [ ] hide the 'Buy more sessions' button from this route /client/calendar
	 
	 Status: Done ✅\
	 Web view ⬇️
	 <img width="1919" height="1031" alt="image" src="https://github.com/user-attachments/assets/a9c71c67-f1a8-46b5-91c4-912b156a86b6" />

	 iOS view ⬇️
 	 <img width="1919" height="1034" alt="image" src="https://github.com/user-attachments/assets/3b0d51c7-90e7-49a0-97be-47e520f655e7" />



	 Additionally i have hidden the similar button from this routes as well\
		- /client/sessions/remaining\
		  	Web view ⬇️
			<img width="1919" height="1034" alt="image" src="https://github.com/user-attachments/assets/788ba84b-d293-4ad8-829d-dc4cc2b011ca" />
			iOS view ⬇️
			<img width="1919" height="1032" alt="image" src="https://github.com/user-attachments/assets/89f1612e-f97f-4a71-b202-2f12cb0c2508" />
		- /purchases\
			Web view ⬇️
			<img width="1919" height="1031" alt="image" src="https://github.com/user-attachments/assets/2ae87fdd-decf-4c61-9212-a846546c3b32" />
			iOS view ⬇️
			<img width="1919" height="1031" alt="image" src="https://github.com/user-attachments/assets/90c1e4f0-3d4a-41b2-a03e-46cc9d22faf0" />




- [ ] Move Pause and Close account to Account settings (main) page:
 	 
	 Status: already done (/client/settings/index). No need to change anything
		<img width="1919" height="913" alt="image" src="https://github.com/user-attachments/assets/82d2dd47-b54a-463a-8a77-b13020441b52" />


- [ ] Guideline 3.1.1 (IAP) — reply, not StoreKit
	 Apple flagged digital products bought outside IAP. The review doc already has the reply: admin-only app, no checkout in iOS, commerce is on the web. 
	 Optional: audit leftover purchase UI so they don’t reject again.

# Coach
- [ ] Move Pause and Close account to Account settings (main) page:
 	Status: already done (/coach/settings). No need to change anything
		<img width="1919" height="1076" alt="image" src="https://github.com/user-attachments/assets/c02d4ceb-2983-46a2-953c-48f6220a572e" />

- [ ] On the plans page, add a box at the bottom with buttons to Pause Account and Close account. These will redirect to the main settings page so people won’t get confused where it went.
	 Status: already done on the website. for iOS we have hidden the plans page. so, nothing to do.
		<img width="1919" height="1029" alt="image" src="https://github.com/user-attachments/assets/c906948f-f77f-48c7-b307-5b7382917118" />


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
	 
	Status: Done ✅\

	***Sessions preview***\
	Web view &darr;
	<img width="2880" height="1800" alt="session-preview-web" src="https://github.com/user-attachments/assets/486cb682-96d2-4a17-9509-bbd038ce7485" />

	iOS view &darr;
	<img width="2880" height="1800" alt="session-preview-ios" src="https://github.com/user-attachments/assets/7b7946a7-12ee-4407-bccd-76075256176e" />
	
	***Offer preview***\
	Web view &darr;
	<img width="2880" height="1800" alt="offer-preview-web" src="https://github.com/user-attachments/assets/8484f045-6c56-4027-85ac-aec92264bcc1" />

	iOS view &darr;
	<img width="2880" height="1800" alt="offer-preview-ios" src="https://github.com/user-attachments/assets/4662ae0e-dc12-439f-bb2f-c68c776418cd" />\
	Package, course, digital product, and membership previews use the same price card + button pattern.


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
