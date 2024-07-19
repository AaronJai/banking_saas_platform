# MoneyMate
A financial SaaS platform that employs finance management, connects multiple bank accounts, real-time transactions and allow money transfers.

# Usage (via deployed link):
On sign-up ensure you follow placeholder format for State, DOB and SSN.
When linking, username is user_good and password is user_pass.
this is using a SANDBOX. Development and Production keys are paid through dwolla.
Chase checking and savings account works best.

# Tech Stack
### Next.js
React framework for server-side rendering, group routes, nested layouts, server actions, etc.

### Horizon
A platform that connects to multiple bank accounts, also displaying real-time transactions and also allows money transfer to other users.
It uses a secure SSR authentication.

### Plaid
For payments, works world-wide, great for banking APIs.

### Appwrite
Used to build our backend
Authentication, databases, functions, storage, messaging, etc.

### Sentry
Application monitoring software that analyses performance and makes our bank more secure
Session Replay - 'get to root cause of an issue by watching replays of real user sessions' 
(removes sensitive data in replay).

### Form management
**Typescript**, **React Hook Form**, **Zod**

### Responsivity - modern responsive UI
**Chart.js** - allows us to create any kind of chart, 
**ShadCN** - component library e.g., simple buttons, alerts, etc.
**TailwindCSS** - utility-first CSS framework; custom styling without having to need separate CSS files

# Features
• **Authentication**: Implement ultra-secure SSR authentication with comprehensive validations and authorization.

• **Connect Banks**: Integrate with Plaid for linking multiple bank accounts.

• **Home Page**: Display an overview of the user account, including total balance across connected banks, recent transactions, and spending by category.

• **My Banks**: Provide a complete list of all connected banks with respective balances and account details.

• **Transaction History**: Offer pagination and filtering options to view transaction history across different banks.

• **Real-time Updates**: Reflect changes across all relevant pages when new bank accounts are connected.

• **Funds Transfer**: Enable users to transfer funds using Dwolla, including required fields and recipient bank ID.

• **Responsiveness**: Ensure the application adapts seamlessly to various screen sizes and devices, providing a consistent user experience on desktop, tablet, and mobile platforms.

This is a [Next.js](https://nextjs.org/) project bootstrapped with [`create-next-app`](https://github.com/vercel/next.js/tree/canary/packages/create-next-app).

## Usage (locally):

Follow these steps to set up the project locally on your machine.

**Prerequisites**

Make sure you have the following installed on your machine:

- [Git](https://git-scm.com/)
- [Node.js](https://nodejs.org/en)
- [npm](https://www.npmjs.com/) (Node Package Manager)

**Cloning the Repository**

```bash
git clone https://github.com/AaronJai/moneymate
cd moneymate
```

**Installation**

Install the project dependencies using npm:

```bash
npm install
```

**Set Up Environment Variables**

Create a new file named `.env` in the root of your project and add the following content:

```env
#NEXT
NEXT_PUBLIC_SITE_URL=

#APPWRITE
NEXT_PUBLIC_APPWRITE_ENDPOINT=https://cloud.appwrite.io/v1
NEXT_PUBLIC_APPWRITE_PROJECT=
APPWRITE_DATABASE_ID=
APPWRITE_USER_COLLECTION_ID=
APPWRITE_BANK_COLLECTION_ID=
APPWRITE_TRANSACTION_COLLECTION_ID=
APPWRITE_SECRET=

#PLAID
PLAID_CLIENT_ID=
PLAID_SECRET=
PLAID_ENV=
PLAID_PRODUCTS=
PLAID_COUNTRY_CODES=

#DWOLLA
DWOLLA_KEY=
DWOLLA_SECRET=
DWOLLA_BASE_URL=https://api-sandbox.dwolla.com
DWOLLA_ENV=sandbox

```

Replace the placeholder values with your actual respective account credentials. You can obtain these credentials by signing up on the [Appwrite](https://appwrite.io/?utm_source=youtube&utm_content=reactnative&ref=JSmastery), [Plaid](https://plaid.com/) and [Dwolla](https://www.dwolla.com/)

**Running the Project**

```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser to view the project.
