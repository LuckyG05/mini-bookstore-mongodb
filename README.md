# Mini Bookstore – MongoDB Project

This project demonstrates converting a relational model into MongoDB's document model.

## Features
- Document based schema
- Embedded reviews
- Schema validation
- MongoDB queries
- Referencing (users → books)

## Database Structure

### books collection
- title
- author
- price
- reviews (embedded)

### users collection
- name
- email
- purchased_books (referencing)

## Sample Queries

Find books cheaper than 450:
```bash
{ price: { $lt: 450 } }
```

Find books with 5 star rating:
```bash
{ "reviews.rating": 5 }
```

Find user who purchased Atomic Habits:
```bash
{ purchased_books: "Atomic Habits" }
```

## Tech Used
- MongoDB Atlas
- Document Data Modeling
