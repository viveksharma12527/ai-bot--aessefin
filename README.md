

# Italian AI Chatbot - Payroll Loan Assistant

An intelligent Italian-language chatbot designed to assist customers with payroll loan applications. The chatbot gathers essential information and guides users through the document submission process for loan assessment.

## Project Overview

This chatbot is built for the banking sector, specifically for handling payroll loan inquiries. It features:

- **Natural Italian Conversation**: Human-like, professional interactions in Italian
- **Multi-Industry Support**: Customizable for Banking, Fashion, and Hospitality sectors
- **Smart Document Collection**: Guides users through required documentation based on their profile
- **Intelligent Validation**: Handles different customer profiles (employees, pensioners, etc.)

## Chatbot Behavior

### Objective
Gather essential customer information and request necessary documents for payroll loan assessment.

### Conversation Style
- Uses random Italian names (Stefano, Giuseppe, Erika, Sara) chosen at session start
- Mirrors the customer's formality level (formal "Lei" or informal "Tu")
- Short, clear messages with only relevant content
- One request per message, no automatic follow-ups

### Initial Greeting
*"Good morning and welcome to the chat. I'm [NAME] from the Cofidis Bank branch. Let's proceed with the assessment. Can you tell me your first and last name?"*

### Information Collection Flow
1. **Work Situation**: "Can you tell me about your work situation?"
2. **Loan Amount**: "And how much would you need?"
3. **Purpose**: "Do you have a particular project or need to fulfill?"

### Loan Amount Rules
- **< €3,000**: "We currently provide financing from €3,000 and up."
- **≥ €3,000**: Proceed with document requests

### Document Requirements

**For Employees:**
- ≤ €10,000: Latest pay stub required
- \> €10,000: Latest paycheck required

**For Pensioners:**
- ≤ €10,000: CUD or Obis-M form required
- \> €10,000: CUD or Obis-M form required

**Non-Fundable Profiles:**
- VAT number/sole proprietorship
- Undeclared work
- Unemployed
- Pension < €700
- Age > 81

For non-fundable profiles, the chatbot asks about guarantor availability.

### Key Features
- No financial calculations provided (installments, interest, APR)
- Document submission via chat (photos accepted)
- Alternative email: info@aessefin.it
- No in-person office visits
- Professional callback option available

## Run Locally

**Prerequisites:**  Node.js

### Quick Start
1. Set the `API_KEY` in `.env` to your Gemini API key.
2. Run the startup script:
   ```bash
   ./start.sh
   ```
   This will install dependencies, clear any existing processes on ports 3001/5173, and start both the backend and frontend servers.

### Manual Setup
1. Install dependencies:
   `npm install`
2. Set the `API_KEY` in `.env` to your Gemini API key.
3. Start the backend:
   `node server.js`
4. Start the frontend:
   `npm start`
