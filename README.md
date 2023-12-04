<h1>Project Document: Mind Link - Personalized Mental Health Companion 🧠💬</h1>
<h2>Project Overview:</h2>
<p>We are team MindLink. 
Mind Link takes a holistic approach to mental health, leveraging the power of personalization. We recognize the significance of tailored experiences in addressing individual mental health needs. By combining user preferences, behavioral patterns, and expert insights, Mind Link aims to provide a comprehensive solution for mental well-being.

<h2>The Problem: User Engagement Challenge </h2>
<ul>
  <li>1️⃣ Decrease Member Usage after First Free Trial
        Impact: Reduced utilization may translate to lower conversion rates to paid subscriptions.
</li>
  <li>2️⃣ Ineffectiveness of Current Promotional Offers
        Insight: Reevaluate the value proposition of promotions to align with user expectations and needs.</li>
  <li>3️⃣ Limited Post-Trial Communication
        Strategy: Strengthen post-trial communication to highlight continued value and encourage 
        subscription renewals.</li>
</ul>

<h2>Our Solution:</h2>
<p>Mind Link stands out by offering a personalized mental health experience. Our app utilizes data from user interactions, mood tracking, and preferences to curate a customized mental wellness plan. Through targeted recommendations and timely interventions, Mind Link ensures users mental health journey is uniquely theirs. Steps below :
<ol>
<li>
<h3>Utilization of Data for Personalization</h3>
<p>MindLink seamlessly leverages Twilio Segment to collect data across various touchpoints, including:</p>
<ul>
<li><strong>Teleconsultations:</strong> Session duration, topics discussed, doctor-patient rapport.</li>
<li><strong>In-app journeys:</strong> Feature usage, content engagement, app navigation patterns.</li>
<li><strong>Promotional campaigns:</strong> Click-through rates, discount coupon usage, campaign responses.</li>
<li><strong>Eventbrite course sign-ups:</strong> Interest areas, learning preferences, event attendance.</li>
</ul>
<p>While invisible to users like Jane, this data is the foundation of her personalized MindLink experience.</p>
</li>
<li>
<h3>Modern Data Foundation with Segment and Data Lakehouse</h3>
![Solution](https://drive.google.com/uc?id=1ePijsCu8luyPlaqt5lDGF33JyFnIDiRm)
<p>MindLink built a modern data foundation with powerful connections from Twilio Segment.</p>
<ul>
<li>Data flows seamlessly into the lakehouse, a central repository for all user information.</li>
<li>This unified view empowers advanced analytics and personalizations, unlike siloed data systems.</li>
</ul>
</li>
<li>
<h3>Composable Customer Data Platform</h3>
![CDP](https://drive.google.com/uc?id=1eTnbSDTypS0TSMck4NznUSz0do7587gO)

<p>MindLink leverages Databricks and AWS to build a robust data management platform.</p>
<ul>
<li>This "composable" approach allows for flexible integration of various data sources and tools.</li>
<li>It enables advanced use cases like:</li>
<ul>
<li><strong>Multi-touch attribution:</strong> Understand the impact of different marketing channels on user behavior.</li>
<li><strong>Customer segmentation:</strong> Group users with similar needs and preferences for targeted interventions.</li>
</ul>
</ul>
<p>Relevant datasets used (mock, historical, and event data) include:</p>
 <ul>
    <li>campaign_desc (Mock)</li>
    <li>campaign_table (Mock)</li>
    <li>causal_data (via Twilio Segment)</li>
    <li>coupon (Mock)</li>
    <li>coupon_redempt (via Twilio Segment)</li>
    <li>user_demographic (Mock)</li>
    <li>product (Mock)</li>
    <li>transaction_data (Mock)</li>
    <li>events_stream (via Twilio Segment)</li>
</ul>
<p>Raw data resides on Amazon S3 (bronze layer), undergoes transformations (silver layer), and finally, clustering creates golden profile views (gold layer).</p>
</li>
<li>
<h3>Advanced Personalization Using Clustering Algorithms</h3>
<p>Aggregated information from Twilio Segment is analyzed using clustering algorithms, like the AutoML feature in Databricks, to create distinct customer profiles.</p>
<ul>
<li>This goes beyond basic demographics, uncovering hidden patterns in user activity, sales, and campaign data.</li>
<li>These insights form the basis for personalized promotions and user journeys.</li>
</ul>
</li>
<li>
<h3>Creation of Customer Personas for Targeted Marketing</h3>
<p>By analyzing user data, MindLink understands household behavior and builds comprehensive customer personas.</p>
<ul>
<li>These personas inform personalized promotions, content recommendations, and app features across various touchpoints.</li>
<li>For example, a new user might receive a welcome email with resources specific to their identified persona.</li>
</ul>
</li>
<li>
<h3>Syncing Customer Personas with Upstream Destinations</h3>
<p>Twilio Segment's Revere ETL seamlessly syncs generated customer personas.</p>
<ul>
<li>The lakehouse acts as the source, and various destinations, like email marketing tools, receive updated profiles.</li>
<li>MindLink uses Salesforce Marketing Cloud to send personalized emails based on individual user personas.</li>
<li>Golden profiles are also synced with the Practice Management System, enhancing the consultation experience for both users and practitioners.</li>
<li>This continuous feedback loop allows for ongoing refinement of user segmentation, personalization, and overall user experience.</li>
</ul>
</li>
<li>

<h3>User-Centric Approach Exemplified with Jane's Journey (Video)</h3>
- Illustration of the personalized approach using Jane's user journey as an example. 
- Highlights how the app tailors its communication based on individual user profiles and experiences.
 -We have presented a **Flutter** to build the mobile application.

## Challenges we ran into
![Data Silos](https://drive.google.com/uc?id=14euczhtZxltUzy-DwFq1YrD0cxSrz1qP)

During the development process, one of the major challenges was breaking the data silos and secondly Identity resolution when marrying multiple data sources. 

## What we learned

The journey of building Mindlink Care taught us valuable lessons about adaptability and resilience in the face of technological challenges. We gained a deeper understanding of the importance of choosing the right technologies for real-time data analysis and the significance of continuous learning in the rapidly evolving field of AI and machine learning.

## What's next for MindLink  (GenAI usecase):

We aspire to leverage more data sources and GenAI to create a personalized, data-driven user engagement strategy. No more generic push notifications, just nudges that feel like they were crafted just for the user.
<ol>
  <li>
    <h3>Data Orchestration: The Maestro of Mental Wellness</h3>
    <p>Databricks acts as the conductor, harmonizing diverse data sources into a symphony of insights:</p>
    <ul>
      <li><strong>App Usage:</strong> Feature engagement, session duration, frequency, and navigation patterns.</li>
      <li><strong>Self-Reported Data:</strong> Mood surveys, journaling entries, and symptom trackers.</li>
      <li><strong>Biometric Data (optional, with user consent):</strong> Sleep patterns and heart rate variability.</li>
      <li><strong>External Data:</strong> Weather and anonymized social media activity (privacy-preserving).</li>
    </ul>
  </li>
  <li>
    <h3>Gen-AI Feature Engineering: Beyond the Obvious</h3>
    <p>Instead of meticulously crafting features, Gen-AI models automatically extract hidden patterns and insights:</p>
    <ul>
      <li><strong>Temporal Relationships:</strong> Uncover patterns in data sequences, like increased app usage before anxiety spikes.</li>
      <li><strong>Nuanced Sentiment Analysis:</strong> Go beyond basic sentiment to understand emotional context and triggers.</li>
      <li><strong>Personalized User Profiles:</strong> Capture individual patterns and responses to interventions.</li>
    </ul>
  </li>
  <li>
    <h3>Targeted Interventions: Tailored Support Every Step of the Way</h3>
    <p>Leveraging Twilio Segment, we deliver targeted interventions through various channels:</p>
    <ul>
      <li>Push notifications with timely reminders and motivational messages.</li>
      <li>In-app messages offering personalized exercises and coping mechanisms.</li>
      <li>SMS nudges for self-care activities and check-ins.</li>
    </p>
    <p>We meticulously track user engagement and gather feedback through surveys and chat logs, ensuring continuous improvement.</p>
  </li>
  <li>
    <h3>Real-time Data Ingestion for Immediate Insights</h3>
    <p>We're harnessing the power of Kafka pub-sub and Delta Live Tables for near real-time data ingestion and processing of our clickstream feeds. This allows us to react to emerging trends and personalize interventions with minimal delay, maximizing their impact.</p>
  </li>
  <li>
    <h3>Fresh Propensity Scoring: Always One Step Ahead</h3>
    <p>Every week, we utilize Databricks AutoML scheduler to automatically retrain our propensity scoring model with fresh data. This ensures our predictions and interventions remain relevant and effective in the ever-changing landscape of our user base.</p>
  </li>
  <li>
    <h3>Gen-AI for Hyper-Personalization and A/B Testing</h3>
    <p>We're taking personalization to the next level with Gen-AI, crafting dynamic campaigns and A/B testing variations that resonate with individual users.This data-driven approach ensures we deliver the most relevant support at the right time, optimizing user engagement and outcomes.</p>
  </li>
 
</ol>
