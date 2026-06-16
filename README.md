# CGE-P Labs

This repo shows my work as I prepare for the Certified GRC Engineer Practitioner (CGE-P) certification from the GRC Engineering Club. Each lab builds on the last. Every one stands up real cloud infrastructure with Terraform and saves evidence that proves the security controls are in place. No screenshots, the way it is commonly done today, just real proof.

## Why I'm doing this

I am pursuing CGE-P because I want to be an accelerant to my stakeholders, not a speed bump. When it comes to chasing evidence and making sure our security posture matches our say-do ratio, I want to be the person who makes that faster, not the one who slows it down.

## What I hope you take away

You can build this too. Getting into the technical weeds can feel scary, especially if you are someone like me who is redeveloping their hands-on technical acumen. I am showing the work so it feels a little less far off for the next person.

## What's here

**compliant-s3** is a Terraform module that builds an AWS S3 bucket meeting five NIST 800-53 controls, with JSON evidence saved for each one. More labs get added as I work through them.

## The controls and why they matter

Think of the bucket like a house. Each control is a different part of keeping that house safe.
 
- **SC-28, protecting data at rest.** This is the safe inside the house. Even if someone gets through the door, what is inside the safe is scrambled and useless to them. The data is encrypted, so the contents are protected even when the walls are not.
- **AC-3, access enforcement.** This is locking every door and window, not just the front door. The house is not left open to the street, and there is no side entrance someone can slip through. Every way the bucket could be exposed to the public is shut.
- **CM-6, configuration baseline.** This is building the house to a known plan and keeping it that way. Versioning is like taking a photo of each room before you change anything, so you can always put it back the way it was. The required tags are like labeling what you own with your address, so nothing goes missing or unaccounted for. If you've ever moved, I am sure you can relate!
- **AU-3, audit records.** This is the camera at the door. It records who came, who left, and when, so there is always a record of what happened.
- **AU-6, audit review.** The footage is kept in a separate locked box, not in the same room being filmed. That way the record can be trusted, and someone can actually go back and review it.

## How the evidence works

Each lab saves two files. `plan.json` shows what the code intended to build. `state.json` shows what actually got built in AWS. Comparing the two is how the compliance gets proven instead of just claimed. I have placed the evidence under each lab's folder, for example `evidence/lab-2-3/`.

