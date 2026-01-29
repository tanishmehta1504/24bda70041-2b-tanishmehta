# Product Filter Application

A simple product filtering and sorting application built using **Next.js**, **TypeScript**, **Shadcn UI**, and **Tailwind CSS**.  
The application demonstrates reusable components, state management, and responsive UI design.

---

## Code Overview

This project is organized using reusable components and shared TypeScript types to maintain clean and scalable code.

---

## 1. types/index.ts

This file defines common TypeScript types used throughout the application.

### SelectOption
Represents an option in a select dropdown.

- **value** (`string`) – Internal value of the option  
- **label** (`string`) – Text displayed to the user  

---

## 2. components/select-control.tsx

A reusable select dropdown component built using **Shadcn UI**.

### Purpose
Provides a customizable select input with label and grouped options.

### Props
- **selectLabel** – Label text displayed before the select  
- **value** – Currently selected value  
- **onValueChange** – Callback triggered when selection changes  
- **options** – Array of `SelectOption` objects  
- **groupLabel** – Label for the option group  
- **placeholder** – Placeholder text when no option is selected  

### Features
- Uses Shadcn UI `Select` components for consistent design  
- Styled with Tailwind CSS (white background, large text, custom height)  
- Label and select input aligned using Flexbox  

---

## 3. components/product-card.tsx

A card component for displaying individual product details.

### Purpose
Renders product information in a clean and structured card layout.

### Props
- **name** – Product name  
- **price** – Product price  
- **category** – Product category (`electronics`, `clothing`, or others)  

### Features
- Uses Shadcn UI `Card` components  
- Displays product name as a large title  
- Formats price to two decimal places  
- Shows category as a badge:
  - `electronics` → default variant  
  - `clothing` → secondary variant  
- Styled with a white background and subtle border  

---

## 4. app/page.tsx

The main page that handles product filtering and sorting.

### Purpose
Displays a filterable and sortable list of products.

### State Management
- **filterCategory** – Controls filtering by category  
- **sortBy** – Controls sorting order by price  

### Data
The page contains four sample products:
- Two electronics items  
- Two clothing items  

Each product includes:
- `id`
- `name`
- `price`
- `category`

### Features
- Category filter: All Products, Electronics, Clothing  
- Sorting options:
  - Default
  - Price: Low to High
  - Price: High to Low  
- Dynamic filtering and sorting based on user selection  
- Responsive grid layout:
  - 1 column on small screens  
  - 2 columns on medium and larger screens  
- Clean and centered UI layout  

---

## Application Flow

1. User selects a category filter (default: All Products)  
2. User selects a sorting option (default: Default)  
3. Products are filtered based on the selected category  
4. Filtered products are sorted by price if sorting is applied  
5. Results are displayed using reusable `ProductCard` components  

---

## Technology Stack

- **Framework:** Next.js (App Router)  
- **Language:** TypeScript  
- **UI Library:** Shadcn UI  
- **Styling:** Tailwind CSS  
- **State Management:** React `useState` hooks  

---

## Conclusion

This project demonstrates modern frontend development practices including reusable components, client-side state management, responsive layouts, and clean UI design using Shadcn UI and Tailwind CSS.
