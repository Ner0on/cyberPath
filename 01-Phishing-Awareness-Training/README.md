# ISO | IEC 27001 - A.6.3 - Information security awareness, education and training. 
<img width="1280" height="750" alt="Untitled design (2)" src="https://github.com/user-attachments/assets/d0a47f62-9274-4553-895a-085ad3f195b7" />

## Objective

October is traditionally recognized as Cybersecurity Awareness Month.
This initiative is held worldwide, and its purpose is to remind us that the human factor remains the most vulnerable part of any security system.

I was inspired by the idea of turning this global campaign into a practical project: to demonstrate how a phishing awareness training can be organized within a real company or an educational environment.


### Skills Learned
- Implemented security control from Annex A
- Designing and running phishing campaigns
- Creating phishing templates and landing pages
- Configuring SMTP/subdomains and testing deliverability
- Analyzing metrics: deliverability, open/click/report rates
- Post-campaign debrief and user training

### Tools Used
- <a href="https://getgophish.com/"> GoPhish </a> 
 
## Steps 
### Step 1

My project focused on testing human susceptibility to phishing, so I used publicly available government tax portal as part of the scenario.

First, I installed GoPhish on my PC and performed basic configuration. 
Then I registered a domain visually similar to a common email provider for demonstration purposes and used it in the campaign.

![photo_2_2025-10-03_15-57-37](https://github.com/user-attachments/assets/c6e2b132-405c-46ee-ac3d-c5bf6a2fd761)

### Step 2

I needed to copy the source code of a login Web Page to simulate credential-harvesting scenarios.

![photo_3_2025-10-03_15-57-37](https://github.com/user-attachments/assets/3a82658c-6400-4c01-b41f-4b7992080978)

### Step 3

Then I generated a realistic-looking phishing email and added tracking. When recipients open the message I get an "open" event on my dashboard — and if they click the link I get a "click" event.

![photo_4_2025-10-03_15-57-37](https://github.com/user-attachments/assets/071ed35e-95ef-4a36-83be-1de8293814c7)

### Step 4

After that, my final step was to create a group of users to receive the campaign — for this exercise I trained my family, so only family members were included. After launching the campaign, I also sent the test link to myself to validate real-world behaviour. Everything looked realistic; the email and landing page appeared legitimate. 
The only clear red flag was the sender address, which I intentionally made slightly suspicious so recipients could notice it before opening any links — that was the point of this test campaign.

<img width="500" height="350" alt="Untitled design (4)" src="https://github.com/user-attachments/assets/5716a04b-5875-4cee-81fb-ba800ec94fc4" />
<img width="500" height="420" alt="Untitled design (3)" src="https://github.com/user-attachments/assets/c895ba69-2c80-4977-92a8-106ff890705c" />

# Conclusion

0/5 — none of the five family members clicked the link (only me for test). Some immediately messaged me asking if the email was legitimate — great result!
Next time the campaign will be a bit more complex (we’ll use more realistic scenarios and attachments), but everything will be by the book: test data, an agreed scope, and a detailed debrief afterwards. I’ll keep training their detection skills.
