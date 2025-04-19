# TCSS 460 Back-end Project

## Project Description

This project implements a Web API using Node.js/Express, PostgreSQL, and the provided Book Data. The API includes authentication and credentialing routes and provides several endpoints for managing book records.

## Group Members

* Anthony Chapkin
* Zakariye Luqman
* Peter W Madin
* Riley Mansfield

## Requirements

### Authentication
- Complete authentication and credentialing routes
- Password change functionality
- Forgotten password recovery

### Book Management (Credentialed Access Only)
- **Retrieve book records:**
  - All books (with pagination)
  - Book by ISBN
  - Books by author
  - Books by title
  - Books by rating
  - At least one additional retrieval method
- **Create:**
  - Add new book records
- **Update:**
  - Update book ratings
- **Delete:**
  - Delete specific book by ISBN
  - Delete a range or series of books

## Project Components

### Documentation (30%)
- Full API documentation using apidoc.js
- Documentation hosted via GitHub Pages

### Unit Testing (30%)
- Thorough testing of all routes using Postman
- Test collections exported to the ./tests directory

### Implementation (40%)
- Node.js/Express framework
- PostgreSQL database
- Predefined interfaces for HTTP responses

## Getting Started

1. Clone the repository (created from template: https://github.com/UWT-SET-TCSS460-LECTURE-MATERIALS/TCSS460-phase-2.git)
2. Install dependencies
3. Set up PostgreSQL database
4. Run the application

## API Interface Definitions

```typescript
interface IRatings {
  average: number;
  count: number;
  rating_1: number;
  rating_2: number;
  rating_3: number;
  rating_4: number;
  rating_5: number;
}

interface IUrlIcon {
  large: string;
  small: string;
}

interface IBook {
  isbn13: number;
  authors: string;
  publication: number;
  original_title: string;
  title: string;
  ratings: IRatings;
  icons: IUrlIcon;
}
```
