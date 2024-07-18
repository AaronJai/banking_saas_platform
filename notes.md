
## Route groups

Having page.tsx in app only allows us to have a **SINGLE LAYOUT** (a layout is a specific UI you can see across multiple pages, e.g., left side bar),
but may not be included in some e.g., auth pages.

i.e., home page and login/signup page uses a different layout.

This can be implemented using ROUTE GROUPS. E.g.,

app/
  ├─ (auth)/
  │  ├─ login/
  │  │  └─ page.tsx
  │  ├─ signup/
  │  │  └─ page.tsx
  ├─ (root)/
  │  ├─ page.tsx
  │  ├─ profile/
  │  │  └─ page.tsx
  ├─ layout.tsx
  ├─ page.tsx


1. Clean URL Structure: Route group folders like (auth) and (root) are not included in the URL path. For example, /login and /root remain simple and clean.
2. Separate Layouts: You can define different layouts for different parts of your application without nesting them deeply in your directory structure.

3. Route groups are not added to file-based routing.
e.g., you can do /sign-in instead of /auth/sign-in

## Forms
Forms can be tricky but one of the most complex things we'll do.
We build ours using react-hook-form and zod (a great library for form validation)

## Atomic Functions
an atomic transaction is one that either works or doesn't. no in-between.
if it goes through, needs to go through to the end. otherwise fail.
- we cannot create a new user account and then not add to the database.
- we cannot add to database, then not connect to plaid

# Plaid and Dwolla
Plaid connects apps with bankaccounts making it easy to access account info and do things like
verifying identity. Like a middleman that ensures info is shared securely.

Dwolla helps send, receive, and request payments specialising in real-time payments.