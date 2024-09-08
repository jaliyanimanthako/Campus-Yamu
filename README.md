# Campus Yamu: Unlock Your Future!** 

Welcome to **Campus Yamu**, the ultimate web application designed to help **Sri Lankan students** choose the best-suited university degree programs based on their Z-scores, district preferences, and subject streams! 

---

### **Project Overview**

Choosing the right university degree program can be overwhelming with so many options and eligibility criteria. **Campus Yamu** simplifies this process by offering personalized degree recommendations based on Z-scores, district information, and subject preferences, empowering students to make informed decisions.

By utilizing cutting-edge **RAG (Retrieval-Augmented Generation)** models and **LangChain**, we've trained our AI using the **UGC Handbook** to provide tailored recommendations for students. Whether you're aiming for **Engineering, Medicine, Arts**, or another field, Campus Yamu is here to help you make the best choice for your academic journey.

---

### **Problem Description**

A survey of 39 university undergraduates revealed that many Sri Lankan school leavers struggle to find university programs that align with their eligibility and preferences【4†source】. This is especially challenging given the complexity of Z-score cutoffs and the diversity of programs. Students often feel overwhelmed by the sheer number of options, lack of proper guidance, and difficulty accessing real-time information on eligibility.

---

###  **Solution: How Campus Yamu Solves This**

**Campus Yamu** acts as an expert companion, simplifying the selection process for students. Our AI-driven platform analyzes over **300 unique degree programs** in seconds, providing personalized recommendations based on Z-scores, district, and subject preferences. This solution significantly reduces the stress of making uninformed decisions and offers clarity to students about the best-suited programs available to them.

The platform achieves this by:
- **Retrieving relevant program information** from the UGC Handbook and matching it with the student's academic profile.
- **Filtering programs** based on the student's eligibility and location preferences, allowing for more targeted recommendations.
- Presenting **clear and personalized options**, which makes it easier for students to make an informed decision about their future.

---

### 🛠 **Key Features**

- **Z-Score Analysis**: Input your Z-score and district to discover degree programs where you have a higher chance of acceptance.
- **AI-Powered Recommendations**: Using **RAG models**, **LangChain**, and **OpenAI**, our tool provides tailored degree options based on the UGC Handbook.
- **Simple & User-Friendly**: Enter your details and preferences, and let our app handle the rest with ease.

---

###  **Powered By**

#### **Retrieval-Augmented Generation (RAG)**
RAG is an advanced model architecture that enhances response generation by retrieving relevant external data before producing a response. This hybrid model combines retrieval-based and generation-based approaches to produce highly contextual and accurate recommendations.

##### **How RAG Works in Campus Yamu**:
- **Retrieval**: When a user inputs their Z-score, district, and preferences, the RAG model first searches a database extracted from the **UGC Handbook**. This database includes detailed information about available university programs, requirements, Z-scores, and districts.
- **Generation**: After retrieving relevant documents from the database, the generation component of RAG processes the content to create a coherent, context-aware recommendation of degree programs.

**Integration Flow**:
1. A **preprocessing step** parses the UGC Handbook into chunks of relevant text, such as information per degree program.
2. These chunks are indexed using tools like **ElasticSearch** or **FAISS (Facebook AI Similarity Search)** for fast retrieval based on user input.
3. The RAG model retrieves relevant passages and generates a natural language response in the form of degree recommendations.

---

#### **LangChain**
**LangChain** is a framework designed to connect large language models (LLMs) with external data sources, memory, and APIs, creating intelligent, dynamic applications. It streamlines the integration of models like **RAG** with various data layers and external knowledge bases.

##### **How LangChain is Used in Campus Yamu**:
- **Data Handling**: LangChain manages interactions between the RAG model and the **UGC Handbook** data, organizing retrieved data into meaningful segments.
- **Chain of Thought**: LangChain ensures coherent, multistep dialogue and reasoning. After receiving user input, it retrieves the relevant data and passes it to the RAG model for generation.
- **External Integration**: LangChain connects the RAG model to other APIs, such as real-time data updates, without needing to change the system architecture.

**Integration Flow**:
1. **LangChain** manages the retrieval logic by controlling the flow of data between the user inputs, the RAG model, and the UGC Handbook.
2. For each query, LangChain first ensures that relevant Z-score and program data are retrieved. It then helps pass this data efficiently to the RAG model for personalized generation.

---

#### **OpenAI**
**OpenAI** provides the underlying language model that powers the natural language generation and understanding capabilities in **Campus Yamu**. **GPT-4** (or a similar model) ensures that the generated responses are fluent, context-aware, and accurate.

##### **How OpenAI is Used in Campus Yamu**:
- **Language Model**: OpenAI’s GPT model generates detailed, human-like text responses. Once the relevant program information is retrieved by the RAG model, GPT processes it to generate degree recommendations in an easily understandable format.
- **Context Awareness**: GPT uses the user’s input along with the retrieved program data to ensure the response is tailored to the individual’s specific academic profile, including Z-score, preferred university, and subject preferences.
- **Preventing Hallucination**: OpenAI’s GPT, when combined with RAG and LangChain, ensures that recommendations are always grounded in actual data from the UGC Handbook, avoiding hallucinations or out-of-context responses.

**Integration Flow**:
1. After LangChain retrieves the relevant Z-score, district, and program data, the **OpenAI GPT** model generates a personalized response.
2. GPT ensures fluency and accuracy in the recommendations and adapts to any follow-up queries or clarification requests by the user.

---

###  **Business Model: Why Campus Yamu Will Succeed**

Campus Yamu is designed with a sustainable business model that ensures growth and success in the Sri Lankan education market. With over **200,000 school leavers** annually【4†source】, there is a massive demand for tools like Campus Yamu. Here’s why it works:

1. **Target Audience**: The platform is geared towards the 200,000 students who leave school each year and are in need of clear guidance on university programs.
2. **Cost-Effective Operations**: The cost structure includes essential expenses like cloud hosting, business registration, marketing, and GPU usage for AI computations. Annual operating costs are projected to be **LKR 2,400,000** (approximately USD 8,000)【4†source】.
3. **Revenue Generation**: We plan to generate revenue by offering listing services for **private university programs**. These institutions can feature their degree programs on the platform for a fee, creating a win-win scenario where students discover alternative education options while we maintain sustainable income streams【4†source】.
4. **Market Penetration**: Campus Yamu will be promoted through **student referrals**, **social media**, **school newsletters**, and participation in university career guidance fairs【4†source】.

**Future Growth Opportunities**:
- **Expansion to Private Universities**: By offering private institutions the opportunity to feature their programs, we broaden the choices for students while generating additional revenue.
- **Counseling Integration**: Adding a personalized counseling feature to connect students with university advisors further enhances the value of the platform.

---

###  **How It Works**

1. **Input Your Details**: Enter your Z-score, district, subject stream, and other preferences.
2. **Get Recommendations**: Our AI, powered by **RAG**, **LangChain**, and **OpenAI**, analyzes the UGC Handbook to find degree programs that match your profile.
3. **Explore Your Options**: Review the recommended programs and choose the one that best fits your aspirations and academic goals.

---

###  **Installation & Setup**

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/yourusername/campus-yamu.git
   ```

2. **Install Required Packages**:
   ```bash
   pip install -r requirements.txt
   ```

3. **Run the Web Application**:
   ```bash
   python app.py
   ```

4. **Access the App**: Open your browser and navigate to `http://localhost:5000`.

---

### **Future Enhancements**

- **Personalized Counseling**: Adding features to connect students with university counselors for additional guidance.
- **Mobile App Integration**: Expanding the web app to mobile platforms to increase accessibility.
- **Real-time Updates**: Incorporating the latest **UGC Handbook** updates and university news.

---

### **Campus Yamu Insights**

Our solution is based on the **Campus Yamu** approach, which provides top university options based on eligibility and preferences. Key features include:
  
- **300+ Programs**: The AI analyzes over 300 unique programs and their requirements to match student profiles【4†source】.
- **User-Friendly Interface**: Students can easily enter preferences and scores, receiving quick, tailored recommendations.
- **Wide Audience**: Targeting over 200,000 school leavers each year ensures scalability and reach【4†source】.

