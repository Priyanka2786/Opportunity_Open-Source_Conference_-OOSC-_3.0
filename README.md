# Opportunity_Open-Source_Conference_-OOSC-_3.0
Opportunity Open-Source Conference (OOSC) 3.0 is a premier event dedicated to fostering innovation, collaboration, and learning in the open-source community.


HACKATHON
                                                                            
For
 Conversational Agent Framework for
 Customer Onboarding
Table of Contents
 Contents
 Document Control.......................................................................................................2
 1. Objective...........................................................................................................4
 2. Core Components................................................................................................4
 2.1 Conversational Agent......................................................................................4
 2.2 Configurable Question Framework....................................................................4
 2.3 Data Orchestration Layer................................................................................5
1. Objective
 To design and develop a configurable conversational agent framework that allows 
users to interact in natural language (voice/text), provide required details, upload 
documents, and complete onboarding journeys seamlessly.
 The framework can be configured for different question set based on customer journey.
 2. Core Components
 2.1 Conversational Agent
 
 
 
 
 
 Supports human-like interactions in natural language (voice/text).
 Multi-channel support: Web, Mobile 
Vernacular Support – Agent can talk in native Indian language
 Configurable conversation flows (per Unique Param).
 Handles context management, error handling, and guided inputs.
 2.2 Configurable Question Framework
 Supports 5 primary types of questions:
 a. User Input (voice/text entry)
 
 
 Collects free-text or structured responses.
 Provides validation (e.g., numeric, date, regex).
 b. Document Upload & OCR API Integration
 
 
 
 Allows user to upload documents (ID, income proof, etc.).
 Calls OCR API to extract data in JSON format.
 Auto-populates extracted fields into conversation.
 c. Third-Party API Integrations
 
 Supports configurable integrations like:
 o Bureau check
 o eKYC (Aadhaar, PAN, etc.)
 o Any other external verification APIs
 d. Photo Capture with Liveliness Detection
 
 
 Captures user’s live photo/selfie.
 Validates authenticity via liveliness check API.
 e. OTP Verification
 
 Generates and validates OTP for mobile/email authentication.

 Ensures secure verification flow.
 2.3 Data Orchestration Layer
 
 
 
 
 
 Collates all captured data (from inputs, OCR, APIs, photos, OTP).
 Applies master data mapping (e.g., converts selected values to system IDs).
 Prepares a unified payload.
 Calls Core System API to push data into backend systems.
 Logs all transactions for audit.
 Project Flow
 We will begin this project in a phased approach. Step A is the first milestone and must 
be completed as part of the hackathon. The subsequent phases of the project will build 
on this foundation.
 Tech Stack
 
 
 
 The Agent should be designed using LangGraph.
 MongoDB as back end : All the conversation data & extracted data points should 
be kept here.
 Configurable questions – All the questions should be configurable and should be 
kept in the DB or some config file.
 Key Requirements
 
 
 
 
 The agent should interact in a natural, human-like manner while collecting 
information from the customer.
 If the conversational bot misunderstands any response, it should explicitly ask the
 customer to verify.
 o If the customer confirms the bot’s interpretation is incorrect, the bot must 
re-collect the data accurately.
 The conversation should remain smooth, user-friendly, and resilient against 
errors.
 Bot should work in vernacular language.  To start with, we can pick English and 
Hindi.
Sample Conversation
 Agent: Hello! I’m here to help you apply for your loan. I’ll just ask you a few quick 
questions, and we’ll be done in a few minutes. Ready to begin?
 Customer: Yes, let’s go.
 Step 1 – Personal Details
 Agent: Great! Can I have your full name as per your official documents?
 Customer: Rohan Mehta.
 Agent: And your date of birth?
 Customer: 15th August 1992.
 Agent: Gender?
 Customer: Male.
 Agent: Which mobile number should we use to contact you?
 Customer: 9876543210.
 Agent: And your email address?
 Customer: rohan.mehta@gmail.com.
 Checkpoint Confirmation – Personal Details
 Agent: Just to confirm, here’s what I have:
 Name: Rohan Mehta
 DOB: 15-Aug-1992
 Gender: Male
 Mobile: 9876543210
 Email: rohan.mehta@gmail.com
 Is that correct?
 Customer: Yes, that’s right.
 Step 2 – Other Details
 Agent: What’s your current residential address?
 Customer: 24, Green Park, New Delhi – 110016.
Agent: Is this owned, rented, or provided by your employer?
 Customer: Rented.
 Agent: How long have you been staying here?
 Customer: 3 years.
 Agent: Do you have a different permanent address?
 Customer: Yes, my permanent address is 56, Rajendra Nagar, Lucknow – 226004.
 Agent: What’s your monthly net income after deductions?
 Customer: 85,000.
 ₹
 Agent: Which bank account should we use for loan disbursement?
 Customer: HDFC Bank, Connaught Place branch.
 Agent: Can you confirm the account number and IFSC code?
 Customer: 123456789012, HDFC0001234.
 Checkpoint Confirmation – Other Details
 Agent: Just to confirm, here’s what I have:
 Current Address: 24, Green Park, New Delhi – 110016 (Rented, 3 years)
 Permanent Address: 56, Rajendra Nagar, Lucknow – 226004
 Monthly net income : 85,000
 ₹
 Account No: 123456789012
 Bank : HDFC Bank, Connaught Place branch.
 IFSC Code: HDFC0001234
 Shall I go ahead with these details?
 Customer: Yes, please.
 Agent: Perfect! Your loan application is now submitted. We’ll review it and get back to you 
shortly with the next steps. Thank you for your time, Rohan!
 Customer: Thank you!
