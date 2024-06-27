# Title

Book store application

## Objective

    Build an application that allows users to browse and search for books, view book details, add books to a shopping cart, and place an order.

## Tech Stack

    React JS

## Completion Instructions

### Functionality

#### Must Have

- Build a ReactJS application with multiple pages/components, including Home, Book Listing, Book Details, Shopping Cart, and Checkout pages.

- Implement features such as book search, book filtering, adding to cart, removing from cart, and order placement.

#### Nice to Have

    List the bonus features or tasks mentioned in the Assignment, if any

#### Pages

    * Page: Home
        Page Details:
            Header: Links for pages Home, Book List, Cart
            Banner: Heading, description and "Explore Books" button
            Few products:   6 Product cards with link.
        Navigation:


    * Page: Book List
        Page Details:
            Header: Links for pages Home, Book List, Cart
            Book Items (title, subtitle, image, price), Search (by title, author), Filter (by price )
        Navigation:
            ."Book List" link in Header
            ."Explore books" button in Home page
            ."Back" button in Book Details page


    * Page: Book Details
        Page Details:
            Book detailed Info (title, subtitle, image, description, price), “Add to cart” Button, "Back" button
        Navigation: Each book link in the book List page

    * Page: Cart
        Page Details:
            Cart Items (title, subtitle, image), “Remove” Button, Checkout Button, Order Summary
        Navigation:
            .‘Cart’ link in Header
            . Back button in Checkout page


    * Page: Checkout
        Page Details: ‘Back’ button, Order Form(personal details, summary, ‘Place Order’ button )
        Navigation: Checkout button in Cart

    * Page: Contact Us
        Page Details: Address Card, Message form,  Footer
        Navigation: Contact Us link in Header



### Guidelines to develop a project

#### Must Have

~ Utilize GitHub

- Commit code regularly and commit messages should be clear
- Include a README file explaining the project setup, usage instructions, and any additional information
- The repo should be well organized and easy to understand.
- The code should be clean, modular, and well-structured
- The application should be visually appealing.
- The application should handle all the errors.

#### Nice to Have

    List the additional/suggested guidelines to follow while developing the project, mentioned in the Assignment, if any

### Submission Instructions

#### Must Have

    List the Instructions to follow while submitting the project mentioned in the Assignment, if any

#### Nice to Have

    List the suggested instructions to follow while submitting the project mentioned in the Assignment, if any

## Technical Details

### Routes

| Page         | Route        | Path       |
| ------------ | ------------ | ---------- |
| Home         | Home         | /          |
| Book List    | Book List    | /books     |
| Book Details | Book Details | /books/:id |
| Cart         | Cart         | /cart      |
| Checkout     | Checkout     | /checkout  |
| Not Found    | Not Found    | /not-found |

### Routes & Components

**Home**

| Component | Details                                          | state              | API (IT Bookstore) |
| --------- | ------------------------------------------------ | ------------------ | ------------------ |
| Home      | Heading, Description, and "Explore books" button | -                  | -                  |
| Header    | Links for pages Home, Book List, Cart            | (Context Consumer) | -                  |

**Book List**
| Component | Details | state | API (IT Bookstore) |
|-------------|--------------------------------------------------|--------------------------------------|--------------------|
| Book List | | apiStatus, booksData, priceRangeValue| /new |
| Header | links for pages Home, Book List, Cart | - | - |
| SearchInput | Search (by title, author) | searchInputValue | /search/{query} |
| PriceRange | Filter (by price) | - | - |
| BookItem | Book Items (title, subtitle, image, price) | - | - |
| Loader | | - | - |
| ErrorMessage| | - | - |

**Book Details**

| Component    | Details                                                                                                           | State                      | API (IT Bookstore) |
| ------------ | ----------------------------------------------------------------------------------------------------------------- | -------------------------- | ------------------ |
| BookDetails  | Book detailed Information - image, title, subtitle, price, description, etc., “Add to cart” Button, “Back” button | apiStatus, bookDetailsData | /books/{isbn}      |
| Header       | links for pages Home, Book List, Cart                                                                             | -                          | -                  |
| Loader       |                                                                                                                   | -                          | -                  |
| ErrorMessage |                                                                                                                   | -                          | -                  |

**Cart**

| Components | Details                                                         | State              | API (IT Bookstore) |
| ---------- | --------------------------------------------------------------- | ------------------ | ------------------ |
| Cart       | Cart Items, “Remove” Button, Order Summary, “Checkout” Button   | (Context Consumer) | -                  |
| Header     | links for pages Home, Book List, Cart                           | -                  | -                  |
| CartItem   | Book Detailed Info (image, title, subtitle, price, description) | (Context Consumer) | -                  |

**Checkout**

| Components      | Details                                                                                                      | State                        | API (IT Bookstore) |
| --------------- | ------------------------------------------------------------------------------------------------------------ | ---------------------------- | ------------------ |
| Checkout        | “Back” button                                                                                                | (Context Consumer)           | -                  |
| UserDetailsForm | Order Form - Personal Details - First Name, Last Name, Email, Mobile No. , Place Order Button, Order Summary | userDetails, isFormSubmitted | -                  |

**Not Found**

| Components | Details                               | State  | API (IT Bookstore)                    |
| ---------- | ------------------------------------- | ------ | ------------------------------------- |
| NotFound   | -                                     | -      | -                                     |
| Header     | links for pages Home, Book List, Cart | Header | links for pages Home, Book List, Cart |

**App**

| Component | Details | State                                                                     | API (IT Bookstore) |
| --------- | ------- | ------------------------------------------------------------------------- | ------------------ |
| App       | -       | cartList (Context Provider), Context: cartList, addToCart, deleteFromCart | -                  |

## Resources

### Design files

    Home, Books Lists, Book Details, Shopping Cart, Checkout
    Reference: https://www.crossword.in/

### APIs

    Books, Book Details, Search
    API reference: https://api.itbook.store/

### Third-party packages

    React Router (react-router-dom)
    Icons (react-icons)
    Loader (react-loader-spinner)
    Range slider (rc-slider)
