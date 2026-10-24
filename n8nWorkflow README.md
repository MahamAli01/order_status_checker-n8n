<div align="center">

# 📦 Order Status Checker — n8n Automation

### An Automated Order Lookup Workflow Using n8n

![n8n](https://img.shields.io/badge/Automation-n8n-orange)
![Workflow](https://img.shields.io/badge/Workflow-Order%20Management-blue)
![Status](https://img.shields.io/badge/Project-Completed-success)
![Level](https://img.shields.io/badge/Level-Beginner-brightgreen)

**A beginner-friendly workflow that checks order IDs and returns the corresponding order status automatically.**

</div>

---

## 📌 Project Overview

The **Order Status Checker** is a workflow automation project built using n8n. It allows a user to submit an Order ID through a form and receive a corresponding order status.

The workflow uses conditional logic to identify different orders and return an appropriate message.

This project demonstrates how workflow automation can simplify repetitive tasks and improve customer support processes.

> **Note:** This project uses sample order records and predefined statuses. It is not connected to a live order management system.

## 🎯 Learning Objectives

* Understand visual workflow automation using n8n.
* Configure a form trigger to collect user input.
* Process form data using Edit Fields nodes.
* Use If nodes to evaluate conditions.
* Create multiple conditional branches.
* Handle unknown order IDs.
* Test and debug workflow executions.
* Understand how automation can support customer service.

## ✨ Features

* **Order ID Input:** Accepts an Order ID through a form.
* **Automated Status Lookup:** Checks the submitted ID against predefined conditions.
* **Conditional Routing:** Routes data through True and False branches.
* **Multiple Order Statuses:** Supports Shipped, Processing, and Delivered.
* **Not Found Handling:** Returns a helpful message for unrecognized IDs.
* **Automated Responses:** Produces a structured output containing the order ID, status, and message.

## 🛠️ Technologies Used

| Technology   | Purpose                                        |
| ------------ | ---------------------------------------------- |
| n8n          | Workflow automation platform                   |
| Form Trigger | Collects the Order ID                          |
| Edit Fields  | Sets and prepares output fields                |
| If Node      | Checks order IDs and controls workflow routing |
| JSON         | Represents structured order information        |

## ⚙️ Workflow Architecture

```text
On Form Submission
        |
        v
    Edit Fields
        |
        v
   If: ORD101?
     /       \
  True       False
    |           |
    v           v
  Shipped    If: ORD102?
               /      \
            True      False
              |          |
              v          v
         Processing   If: ORD103?
                       /       \
                    True       False
                      |           |
                      v           v
                  Delivered    Not Found
```

## 📋 Sample Test Cases

| Order ID | Expected Status | Expected Result                                                  |
| -------- | --------------- | ---------------------------------------------------------------- |
| `ORD101` | Shipped         | Your order has been shipped!                                     |
| `ORD102` | Processing      | Your order is being processed.                                   |
| `ORD103` | Delivered       | Your order has been delivered!                                   |
| `ORD999` | Not Found       | Sorry, we could not find your order. Please check your Order ID. |

All four test cases were successfully tested during development.

## 🔄 How It Works

1. The user opens the Order Status Checker form.
2. The user enters an Order ID.
3. The form trigger receives the submitted information.
4. Edit Fields prepares the data for processing.
5. The first If node checks whether the ID matches `ORD101`.
6. If it does not match, subsequent If nodes check `ORD102` and `ORD103`.
7. The matching branch returns the appropriate status and message.
8. If no condition matches, the workflow returns a Not Found response.

## 🚀 Future Improvements

Possible enhancements include:

* Connect Google Sheets to store and retrieve order records.
* Replace hardcoded order IDs with dynamic database lookups.
* Connect the workflow to an external e-commerce API.
* Send order updates through email or messaging applications.
* Add validation and improved error handling.
* Build a customer-facing interface for order tracking.

## 🧠 Skills Practiced

* Visual workflow design
* Conditional logic
* Form handling
* Data transformation
* Workflow debugging
* Test-case validation
* Basic customer service automation

## 📚 Learning Outcomes

Through this project, I learned how to build and test an automation workflow in n8n, process form submissions, route data using conditional branches, and return different results based on user input.

This project is a foundation for more advanced integrations involving Google Sheets, webhooks, APIs, and AI-powered customer support.

## 👩‍💻 Student Information

**Project:** Order Status Checker
**Category:** Workflow Automation
**Platform:** n8n
**Level:** Beginner
**Purpose:** Learning and portfolio development

---

<div align="center">

**Built as a hands-on project while learning workflow automation with n8n.**

</div>
