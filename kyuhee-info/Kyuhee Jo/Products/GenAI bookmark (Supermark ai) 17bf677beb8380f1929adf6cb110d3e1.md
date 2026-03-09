# GenAI bookmark (Supermark.ai)

Description: GenAI-enabled web bookmarks
Status: Shipped
Tags: GenAI
Role: Product manager
When: June 6, 2023

# TL;DR

Back when ChatGPT was still new, and when it did not have the ability to search the internet, I worked with a team of engineers to develop a GenAI enabled bookmark. It was basically a chrome extension that allowed users to clip webpages into a knowledge base, and chat with the “bookmarks” using ChatGPT. We formally deployed and shipped the product after the AI X Product hackathon in which “Supermark” was born. In fact, our [launch on LinkedIn](https://www.linkedin.com/posts/kyuheejo_chatgpt-chatgpt-gpt-activity-7082347235945971712-nGfu?utm_source=share&utm_medium=member_desktop) was quite successful, generating 30,000+ impressions and gaining 100+ signups. However, despite our effort to [sell it as a B2B enterprise software](https://psychadelic-centaur-6776.typedream.app/)  we failed to monetize the product, and the project is no longer maintained.  

# Version 1 (from AI X Product hackathon)

[https://youtu.be/1ymM8s_Q13c?si=brwBMcM9gQr5HOFM](https://youtu.be/1ymM8s_Q13c?si=brwBMcM9gQr5HOFM)

# Version 2

[https://www.loom.com/share/61541afb9d234a0f8d81078930d853fb](https://www.loom.com/share/61541afb9d234a0f8d81078930d853fb)

[https://youtu.be/bWkILFzM0JE?si=o1FrT0nDuWtNC5Gl](https://youtu.be/bWkILFzM0JE?si=o1FrT0nDuWtNC5Gl)

![demo_supermark.gif](GenAI%20bookmark%20(Supermark%20ai)/demo_supermark.gif)

## Product Overview

Bookmark.ai (now Supermark) is a browser extension designed to enhance internet navigation by allowing users to bookmark pages with a single click. These bookmarks are indexed and embedded using OpenAI text embeddings, enabling semantic search and personalized, up-to-date responses. It leverages AI to create a powerful tool for storing, retrieving, and summarizing web content.

---

## Problem Statement

Modern internet users often struggle with managing their browsing history and bookmarks. The following issues highlight this pain point:

1. **Tab Overload**: Users often keep multiple tabs open, leading to decreased device performance and cognitive overload
2. **Disorganized Bookmarks**: Traditional bookmarking tools offer limited organization, making it difficult to retrieve saved content
3. **Inefficient Information Retrieval**: Scrolling through browsing history or an unstructured bookmark list is time-consuming and ineffective

---

## Objectives

Bookmark.ai aims to:

1. Simplify the bookmarking process to a single click
2. Enable powerful semantic search functionality to retrieve relevant bookmarks easily
3. Provide a ChatGPT-like interface to generate contextual answers using user-collected documents
4. Offer source document references for transparency and validation

---

## Key Features

1. **Single-Click Bookmarking**: Save any webpage instantly via a browser extension
2. **Semantic Search**:
    - Retrieve relevant bookmarks using natural language queries
    - Powered by OpenAI text embeddings for high accuracy
3. **ChatGPT-like Q&A Interface**:
    - Generate contextual answers based on saved bookmarks
    - Use personalized document data for up-to-date responses
    - Display source references for user confidence
4. **Organized Bookmark Management**:
    - Categorize bookmarks by tags, topics, or user-defined folders
    - Filter and sort bookmarks for streamlined navigation
5. **Cross-Device Sync**:
    - Sync bookmarks across devices for seamless access
6. **Privacy and Security**:
    - Encrypt user data to ensure privacy and compliance with security standards

---

## Technical Specifications

### Frontend

- **Framework**: React.js
- **Browser Extension**: Designed for Chrome, with future support planned for Firefox and Safari

### Backend

- **Language**: Python
- **AI Services**: OpenAI APIs for text embeddings and LLM services
- **Database**: LanceDB (vector database for persistence)

### Architecture

- **Data Flow**: Browser extension scrapes and saves user-selected pages to the backend, where they are embedded, indexed, and stored
- **Search Mechanism**: Uses vector similarity to match user queries with indexed bookmarks
- **Response Generation**: Combines indexed data with OpenAI models to generate contextual answers

---

## User Personas

### Persona 1: Busy Professional

- **Pain Points**: Struggles with managing multiple tabs and quickly finding relevant information
- **Solution**: One-click bookmarking and semantic search save time and increase productivity

### Persona 2: Student/Researcher

- **Pain Points**: Needs an organized way to save and retrieve academic resources
- **Solution**: Tags and semantic search enable efficient retrieval of research materials

### Persona 3: Knowledge Enthusiast

- **Pain Points**: Loses track of interesting articles and web pages
- **Solution**: AI-generated summaries and answers from saved content keep learning streamlined

---

## Roadmap

### Phase 1: MVP

- Develop a browser extension for Chrome
- Implement single-click bookmarking and basic semantic search
- Integrate OpenAI embeddings for Q&A functionality

### Phase 2: Enhanced Features

- Add “Chat with PDF” functionality
- Add function to identify a particular source
- Support cross-device functionality

### Phase 3: Scaling and Monetization

- Introduce a freemium model with premium features (e.g., advanced search filters, unlimited bookmarks)
- Optimize backend for scalability and performance
- Explore B2B use cases (e.g., team collaboration tools)

## UI Design on Figma

[https://www.figma.com/design/aIhRcjSWGeUMXS6MAQp4F9/Bookmark.ai?node-id=0-1&t=nbes0ohFsFaZZfXo-1](https://www.figma.com/design/aIhRcjSWGeUMXS6MAQp4F9/Bookmark.ai?node-id=0-1&t=nbes0ohFsFaZZfXo-1)