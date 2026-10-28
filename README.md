# ParentConnect AI

**Student:** Arpit Brijesh Srivastava  
**Candidate registration number:** 1000626  
**School:** Viraj International School  
**CRS:** Artificial Intelligence  
**Project:** ParentConnect AI – School Communication Assistant

## Project overview

Parents often need quick guidance about attendance, examinations, fees, announcements, transport, and school procedures. ParentConnect AI is a friendly chatbot built in **Dialogflow ES** to help them find the right information or identify the appropriate school channel to contact.

The agent export contains **26 intents**, including welcome and fallback intents, **16 custom entities**, and training phrases for different ways parents might ask a question. It uses required parameters, slot-filling prompts, follow-up contexts, suggestion chips, and simple information cards.

## What the chatbot can help with

- Attendance enquiries and guidance on reporting an absence or leave
- Exam schedules and other academic enquiries
- Fee structure, payment options, and due-date enquiries
- School announcements, holidays, and timings
- Transport, location, contact, admissions, and meeting enquiries
- Follow-up questions, changing topics, restarting, and recovering from unclear questions

## Intents

| Intent or group | Purpose |
| --- | --- |
| Default Welcome Intent; Help and Services | Welcome parents and show the available topics. |
| Attendance Enquiry; Attendance Enquiry - yes/no; Report Absence or Leave | Ask for the relevant class, guide attendance enquiries, and handle absence-related follow-ups. |
| Exam Schedule; Academic Information | Identify the exam or academic topic and guide parents to the appropriate information source. |
| Fee Structure; Fee Structure - yes/no; Fee Due Dates and Payment | Ask for the class when needed and handle fee and payment follow-ups. |
| School Announcements; Holidays and Calendar; School Timings | Respond to questions about notices, calendar events, and timings. |
| Transport Information; Location and Directions; Contact Information | Guide parents to transport, directions, and school contact channels. |
| Admissions Enquiry; Teacher or Staff Meeting Request; General School FAQ | Handle admissions, meetings, and common school questions. |
| Switch Topic; Start Over; Thank You and Goodbye | Support conversation transitions and endings. |
| Default Fallback Intent; Default Fallback Intent - Repeat | Help parents recover when their question is not understood. |

## Entities

The agent uses these **16 custom entities** to recognise details in a parent's question:

| Entity | Information recognised |
| --- | --- |
| `class_level` | A child's class or grade |
| `exam_type` | The type of examination |
| `academic_period` | A term, month, or other academic period |
| `academic_topic` | The academic subject of an enquiry |
| `attendance_topic` | The type of attendance question |
| `fee_category` | The category of fees |
| `announcement_category` | The type of announcement |
| `holiday_type` | The type of holiday or break |
| `transport_topic` | The transport information requested |
| `location_topic` | A location or directions enquiry |
| `school_department` | The relevant school department |
| `staff_role` | The staff member or role requested |
| `contact_method` | The preferred way to contact the school |
| `admission_topic` | The admissions question |
| `faq_topic` | The general school question |
| `query_category` | The topic selected when switching enquiries |

## Import into Dialogflow ES

1. Download `ParentConnect_AI_GitHub_Import.zip` from this repository.
2. Open the **Dialogflow ES** console and select a suitable agent or create a new one.
3. Open the agent settings and use **Export and Import → Import from ZIP**.
4. Select the downloaded ZIP and allow the agent to train.
5. Test the intents, required prompts, follow-ups, fallback responses, and rich content in Dialogflow.

The repository ZIP is a public-sharing copy of the agent export with a legacy key removed from its settings.

## Testing and improvements

| Test | Result |
| --- | --- |
| Grade 8 midterm exam | Passed: captured the class and exam type; directed the parent to confirmed school sources. |
| Grade 8 fee due date | Initially failed: matched Academic Information. Passed after adding fee training phrases and tagging “Grade 8” as `class_level`. |
| Fee enquiry → accounts office → attendance | Passed: matched each new topic and captured the relevant department or class. |
| Unclear message → school timings | Passed: gave a fallback, then recovered and matched School Timings. |

## Live chatbot

[Open ParentConnect AI](https://arpitsrivastava-ibcp.github.io/IDAI101-1000626-Arpit-Brijesh-Srivastava/)

Click the chat icon in the bottom-right corner to start. The chatbot helps parents with attendance, exams, fees, and other school enquiries. It does not access live student records or confirmed school schedules.

## Scope and limitations

This chatbot is not connected to a school's private attendance records or live notices. It does not provide verified individual attendance figures, current fee amounts, or confirmed exam dates. When such information is unavailable, it directs parents to official school channels rather than inventing an answer.
