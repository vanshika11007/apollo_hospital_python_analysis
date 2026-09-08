
# 🏥 Apollo Hospitals: Appointment No-Show & Revenue Analytics

## 📌 Project Overview
Missed healthcare appointments (no-shows) create massive logistical bottlenecks, increase wait times for other patients, and cause severe financial losses for medical institutions. This project analyzes a large-scale dataset of hospital appointments to uncover the demographic patterns, booking behaviors, and root causes behind patient no-shows. 

By joining and cleaning Fact (Appointments) and Dimension (Doctors) tables, this analysis extracts actionable business intelligence to help hospital administration optimize scheduling logistics, improve patient engagement, and significantly reduce revenue leakage.

## 📊 Dataset Details
The analysis is built on two primary datasets:
* **Appointments Fact Table (`apollo_appointments_fact.csv`):** 75,000 records detailing individual appointment events, booking channels, lead times, patient demographics, insurance coverage, and operational metrics (wait times, satisfaction).
* **Doctors Dimension Table (`apollo_doctors_dim.csv`):** 320 records containing doctor profiles, including specialties, years of experience, ratings, and consultation fees.

## 🎯 Project Objectives
The primary goals of this data analysis project are to:
1. **Identify No-Show Drivers:** Discover which patient demographics, booking channels, and lead times contribute most to missed appointments.
2. **Quantify Financial Impact:** Calculate the exact amount of revenue lost due to no-shows and identify which departments are hit the hardest.
3. **Evaluate Patient Engagement:** Measure the effectiveness of current reminder systems (SMS, WhatsApp, Calls) and loyalty programs (Apollo Memberships) in improving attendance.
4. **Assess Operational Efficiency:** Analyze doctor utilization rates, patient wait times, and satisfaction scores to identify bottlenecks in daily operations.
5. **Deliver Actionable Recommendations:** Provide data-backed strategies to hospital management to reduce no-shows and optimize resources.

## 💡 Key Business Insights & Findings

### 1. Financial & Revenue Impact
* **🚨 Severe Revenue Leakage:** Identified a staggering **₹1.97 Crore** in lost revenue directly attributed to no-shows. The Dermatology and General Medicine departments experienced the highest financial impact.
* **💳 Insurance & Out-of-Pocket:** Demonstrated that insured patients have significantly lower out-of-pocket expenses, making them much more reliable attendees compared to uninsured patients. 

### 2. Patient Behavior & Risk Factors
* **🤝 Patient Loyalty vs. Risk:** First-time patients carry a massive **~66% no-show risk**, while repeat patients and active Apollo Members drop this cancellation risk to just **~8%**.
* **⏳ Booking Lead Time:** Established a clear mathematical trend demonstrating that longer booking lead times (appointments booked weeks in advance) heavily increase the probability of a patient abandoning the consultation.
* **📱 Engagement Effectiveness:** Proved that proactive patient engagement strategies (bundled automated SMS, WhatsApp, and voice calls) drastically reduce the probability of a no-show compared to unreminded control groups.

### 3. Operational Quality & Doctor Utilisation
* **⚖️ Time vs. Satisfaction:** Revealed a near-zero correlation between consultation duration and patient satisfaction. Spending 40 minutes with a patient does not yield higher ratings than spending 15 minutes.
* **🕒 Wait Time Consistency:** Operational wait times are surprisingly flat at **~11.55 minutes** regardless of the time of day (Morning, Afternoon, or Evening), indicating consistent but rigid operational bottlenecks.
* **📈 Experience Premium:** Confirmed a positive linear trend between a doctor's years of experience and their average consultation fee.

## 🎯 Strategic Recommendations for Management
1. **Dynamic Overbooking:** Implement targeted overbooking (e.g., 10-15%) specifically for first-time patients and long-lead bookings to offset anticipated no-shows.
2. **Aggressive Reminder Protocols:** Mandate multi-channel reminders (SMS + WhatsApp) for all appointments booked more than 7 days in advance.
3. **Loyalty Push:** Incentivize walk-in and first-time patients to sign up for Apollo Memberships at the front desk, as membership drops no-show rates to single digits.

## 🛠️ Tech Stack & Methodologies
* **Language:** Python 3
* **Libraries Used:** 
  * `pandas`: Data manipulation, cleaning, handling nulls, multi-table joins, and advanced aggregations.
  * `matplotlib`: Executive-ready data visualization, custom color mapping, subplots, and zoomed-axis detailing.
* **Environment:** Jupyter Notebook / VS Code

## 📂 Project Structure & Analysis Phases
1. **Master Data Setup:** Merged Fact and Dimension tables on `doctor_id`, resolved duplicate columns, and cleaned status flags.
2. **Business Overview:** Mapped appointment volumes, booking channel mix, and overall completion rates across years and quarters.
3. **No-Show Analysis:** Analyzed dropout rates by medical specialty, patient city, booking lead days, and time of day.
4. **Reminder & Engagement:** Measured the exact impact of prior patient history, membership status, and bundled reminder types.
5. **Patient Demographics:** Grouped high-risk factors by age brackets, gender, and chronic condition presence.
6. **Financial & Operational Impact:** Calculated total revenue leakage, average out-of-pocket costs, doctor utilization rates, and operational wait times.

## 🚀 How to Run the Project
1. Download or clone this repository to your local machine.
2. Ensure you have Python installed along with the required analytical libraries:
   ```bash
   pip install pandas
   pip install matplotlib.pyplot
   pip install numpy
