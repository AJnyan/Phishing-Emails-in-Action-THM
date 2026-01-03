# Phishing-Emails-in-Action-THM

## Task 1: Introduction 

Now that we covered the basics concerning emails in Phishing Emails 1, let’s dive right into actual phishing email samples. 

Each email sample showcased in this room will demonstrate different tactics used to make the phishing emails look legitimate. The more convincing the phishing email appears, the higher the chances the recipient will click on a malicious link, download and execute the malicious file, or even send the prince of some country a wire transfer.

Warning: The samples throughout this room contain information from actual spam and/or phishing emails. Proceed with caution if you attempt to interact with any IP, domain, attachment, etc.

**Questions**

Read the above

  | Answer: No answer needed

## Task 2: Cancel your PayPal order

**Summary**


Techniques used in the email:
  * Spoofed sender address
  * URL shortening services
  * HTML mimicking a legitimate brand (PayPal)
Red flags in the email:
  * Recipient address doesn’t match the actual Yahoo account.
  * Sender name claims to be PayPal (service@paypal.com) but the actual email is unrelated (gibberish@sultanbogor.com).
  * Subject line implies a transaction you may not recognize, prompting urgency (social engineering).
Email content:
  * Designed to look legitimate, mimicking PayPal.
  * No attachments; the main interactive element is a “Cancel the order” button/link.
Link analysis:
  * The button uses a URL shortener, which hides the destination.
  * Investigating the raw HTML revealed the link redirects to google.com, not PayPal.

**Questions**

What phrase does the gibberish sender email start with?

look closely to the email from THM:

<img width="1005" height="155" alt="email1-details" src="https://github.com/user-attachments/assets/7512d42d-2f10-4783-b511-2a3a9b95630d" />

starts with noreply therefore:

  | Answer: noreply

## Task 3: Track your package

This email is a classic example of phishing. It tries to trick you by pretending to be from a mail delivery center, even using a fake tracking number in the subject line to look official. However, there are several red flags:

* Fake Sender: The email address isn't actually from a real delivery service; it's just "spoofed" to look that way.
* Hidden Tracking: Inside the email’s code, there is a tiny, invisible image called Tracking.png. This is a "tracking pixel" that tells the spammer exactly when you open the email.
* Dangerous Links: While the link looks like a tracking number, it actually points to a shady website that could infect your computer with malware.

**Questions**

What is the root domain for each URL? Defang the URL. 

By using this link:

https://gchq.github.io/CyberChef/#recipe=Defang_URL(true,true,true,'Valid%20domains%20and%20full%20URLs')

we can defang the link to prevent it from being accessible.

  | Answer: devret[.]xyz

## Task 4: Select your email provider to view document

* Techniques used in the email:
  * Creates a sense of urgency (e.g., “link expires today”)
  * HTML impersonation of legitimate brands (OneDrive, Adobe)
  * Link manipulation to redirect victims to fake pages
  * Credential harvesting by asking users to log in
  * Poor grammar and typos
* Red flags and observations:
  * Email prompts immediate action with a “download the fax” button.
  * Links redirect to non-Microsoft and non-Adobe URLs despite appearing legitimate.
  * Page titles and branding are faked (e.g., “Share Point Online”) to appear trustworthy.
  * Victims are prompted to log in with their email credentials; credentials are sent to the attacker.
  * Even correct credentials would trigger a fake error message, ensuring the attacker still collects them.
  * Multiple grammatical errors reveal the email is suspicious.
 
**Questions**

This email sample used the names of a few major companies, their products, and logos such as OneDrive and Adobe. What other company name was used in this phishing email?

<img width="834" height="509" alt="email6-details2" src="https://github.com/user-attachments/assets/45d2b88a-a2d2-4288-baa2-f713fd22f15a" />

The screenshot above said "Citrix Attachments" so i just assume "Citrix" was also one of the company.

  | Answer: Citrix

## Task 5: Please update your payment details


* **Techniques used**: Spoofed email address, urgency, HTML impersonation of Netflix, poor grammar/typos, attachments.
* **Sender spoofing**: Appears to be from Netflix Billing, but the actual sender is z99@musacombi.online.
* **Urgency**: Claims the account is suspended, pressuring the victim to act quickly; reinforced throughout the email body.
* **Typos**: Netflix is misspelled multiple times, though not as part of typosquatting.
* **Attachment**: A PDF is included, prompting the victim to “Update Payment Account.”
* **Suspicious details**: The phone number listed is unusual for a US-based Netflix account.
* **Overall**: The email uses urgency, brand impersonation, and a malicious attachment to trick the recipient into interacting and potentially revealing sensitive information.

**Questions**

What should users do if they receive a suspicious email or text message claiming to be from Netflix?

I found my answer inside this article:

https://www.consumeraffairs.com/news/police-warn-of-new-netflix-email-phishing-scam-121718.html

<img width="622" height="85" alt="Screenshot 2026-01-03 at 9 47 37 PM" src="https://github.com/user-attachments/assets/43214a97-4ec8-4261-97dc-54a0aa21bd30" />

screenshot above got the answer:

  | Answer: forward the message to phishing@netflix.com

## Task 6: Your recent purchase

* **Techniques used**: Spoofed email address, BCCed recipient, urgency, poor grammar/typos, and a malicious attachment.
* **Sender spoofing**: The email claims to be from Apple Support, but the real sender is gibberish@sumpremed.com.
* **BCC usage**: The victim wasn’t directly addressed; instead, they were BCCed. The visible “recipient” address is another spoofed Apple‑like address meant to appear legitimate.
* **Urgency**: The message implies action is required, pushing the victim to respond quickly.
* **Typos**: Both the sender and recipient addresses contain clear errors—donoreply and payament—which signal low credibility.
* **Empty body**: There is no email content at all; the entire attempt relies on the victim opening the attachment.
* **Suspicious attachment**: The attached file is a .DOT template file (a Microsoft Word template format), which is unusual in legitimate communications.
* **Attachment contents**: The file displays a large image mimicking an App Store receipt. Its embedded link includes Apple‑related keywords like apps and ios to appear legitimate.

**Questions**

What does BCC mean?

  | Answer: Blind Carbon Copy

What technique was used to persuade the victim to not ignore the email and act swiftly?

*In this context, Urgency is a psychological trick used to make us feel like you need to act right now without stopping to think.
When a scammer uses urgency, they are trying to trigger a "panic response" so you overlook the red flags (like a weird email address or a shady link).*

  | Answer: Urgency

## Task 7: DHL Express Courier Shipping notice.


* Opening the attachment reveals content designed to appear legitimate, but the document executes a payload that results in an error.
* This email demonstrates spoofed sender information, HTML used to imitate DHL, and the use of a malicious attachment.
* The sender address doesn’t match DHL, even though the email claims to be about a package the company is supposedly shipping.
* The body of the email uses HTML to mimic an authentic DHL message.
* When examining the email’s source code, the “view as a web page” link has no actual destination, which is a strong sign of a poorly constructed phishing attempt.
* The only interactive element is the attachment—an Excel file.

**Questions**

What is the name of the executable that the Excel attachment attempts to run?

<img width="978" height="551" alt="email4-attachment3" src="https://github.com/user-attachments/assets/be856ec9-5807-4076-ad52-e8addd42bd57" />

*The answer is in above screenshot*

  | Answer: regasms.exe

## Task 8: Conclusion

In this room, we looked at various phishing samples. 

Some of the samples shared similar techniques whereas, others introduced a new tactic for you to see and learn from. 

Understanding how to detect phishing emails takes awareness training.

Visit the resources below to acquaint yourself with other signs to look out for in phishing emails. 

Additional Resources:
* https://www.knowbe4.com/phishing
* https://www.itgovernance.co.uk/blog/5-ways-to-detect-a-phishing-email
* https://cheapsslsecurity.com/blog/10-phishing-email-examples-you-need-to-see/
* https://phishingquiz.withgoogle.com
  
The next room in this module: Phishing Emails 3

**Questions**

Read the above

  | Answer: No answer needed.

<img width="1280" height="800" alt="Screenshot 2026-01-03 at 9 08 50 PM" src="https://github.com/user-attachments/assets/a0cd7be7-9619-4233-ad8d-ec419a6672ad" />
