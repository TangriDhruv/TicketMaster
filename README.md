# 🎫 TicketMaster Event Discovery System

An Android application that helps users find events happening around them and provides detailed information including Date, Venue, Price Range, and more. Users can search events by Category, Country Code, or explore all events.

---

## 📱 1. Android Application

### 🎨 User Interface Components
- **TextView**: Displays event names, dates, locations, and more
- **EditText**: Input field for searching events
- **RadioButtons**: Choose search type (Category, Country Code, All Events)
- **Button**: Initiate search and view tickets
- **RecyclerView**: Displays the list of events
- **CardView**: Styles event items in the list
- **ProgressBar**: Indicates loading state
- **ScrollView**: Used in details screen for variable content lengths

### 🧑‍💻 User Input
- Search term input (e.g., *Music*, *Dance*, *Sports*)
- Country Code input (e.g., *US*, *UK*, *AU*, *AS*)
- View all available events
- Maximum of **10 search results** shown

### 🌐 HTTP Requests
- Uses **OkHttp** for network requests
- Background execution with `AsyncTask`
- Calls different endpoints depending on search type
- Implements robust error handling

### 🧾 Data Parsing
- Uses **Gson** to parse JSON into Java objects
- Maps responses to Event model
- Handles varied data formats (e.g., dates, prices, locations)

### 📋 Information Display
- **List View**: Event name, date, venue, location
- **Detail View**: Ticket link, pricing, detailed info
- Shows empty/error states appropriately

### 🔁 Repeatable Functionality
- Supports repeated searches
- Toggle between search types
- Navigate to and from detail view seamlessly

### 📷 Demo Screens (Add screenshots in GitHub later)
- Search by **All Events**
- Search by **Category**
- Search by **Country Code**

---

## 🌍 2. Web Service

### 🧩 API Implementation
- RESTful API receives requests from Android app
- Processes `searchType` and `query` parameters
- Fetches data from **Ticketmaster API**
- Returns structured JSON

### ⚙️ Business Logic
- Fetches and filters data from Ticketmaster
- Processes responses to extract needed info
- Supports all search types: category, country, all

### 🔗 Third-Party Integration
- Integrates with **Ticketmaster API**
- Handles XML/JSON parsing, rate limits, and API errors

### 📤 Response Formatting
- Returns clean, structured JSON
- No extraneous data
- Optimized for easy parsing by the app

---

## 📈 3. Logging and Dashboard

### 📝 Information Logged
- Client IP Address  
- Search Type  
- Search Query  
- Timestamp  
- Response Status & Time  
- Number of Results Returned  

### 🗄️ Data Storage
- Logs are saved in **MongoDB**
- Structured format for analytics
- Chronological timestamping for tracking

### 📊 Operations Analytics Dashboard
- Most popular search terms
- Average response time
- Distribution of search types (category, country, all)

### 🔍 Log Display
- Human-readable logs (not raw JSON)
- Historical request/response viewer

---

## 🚀 4. Deployment

- Web service is deployed via **GitHub Codespaces** using Docker
- To run:
  1. Create a new Codespace
  2. Update base URL in the `APIService.java` file in the Android app
  3. Expose the correct port using the **Ports tab** in Codespaces
  4. Make port public
  5. Click the globe icon to get the full URL

---

## ▶️ 5. Run the Application

### 🔧 Android App
1. Download the Android app ZIP:  
   [EventFinderAndroidApp](https://github.com/CMU-Heinz-95702/distributed-systems-project-04-TangriDhruv)
2. Create a Codespace on the repo using the `<> Code` button → **Codespaces** tab → **Create new Codespace**
3. Open **Ports tab** → Right-click → **Make port public**
4. Hover over **Forward Address** column → Click 🌐 Globe icon
5. Copy the exposed URL and **paste it into `APIService.java`** in your Android app
6. Run the Android application

### 🖥️ Web Service (Local)
- Download and unzip `FindMyEventWebservices.zip`
- Open and run the service in **IntelliJ**


