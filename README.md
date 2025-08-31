# CompliSight
A cloud-based compliance monitoring app tailored for small and mid-sized brokers that delivers low-cost, automated compliance tools while ensuring alignment with SEBI’s market integrity &amp; investor protection goals.
Build a full-stack SaaS web application called CompliSight — “Smart, Affordable Compliance for Every Broker”.
The app helps small & medium-sized brokerage firms in the securities sector with low-cost, efficient compliance monitoring, aligned with SEBI’s investor protection and market integrity goals.
🛠 Tech Stack
Frontend: Next.js + TailwindCSS
Backend: Node.js (Express)
Database: MongoDB (Mongoose ORM)
Auth: JWT-based authentication + role-based access (User / Admin)
Deployment: Docker + docker-compose
🔑 Core Features to Scaffold
1. Landing Page (/)
Hero section: headline “Compliance Made Simple for Every Broker”.
Short features (Assessment • Surveillance • Reporting • AI Assistant).
CTA: “Get Started” → login/register.
2. Authentication
User registration & login.
JWT-based sessions.
Role: user (broker firm) / admin (compliance officer).
3. Business Assessment Module (/assessment)
Questionnaire (yes/no, rating scale).
Auto-generate a Risk Score.
Show compliance gaps with recommendations.
Save history in DB.
4. Compliance Surveillance Module (/surveillance)
Sub-tabs:
Trade Surveillance → input trade data (CSV or manual). App flags unusual patterns (wash trades, high volumes).
Employee Trades → record employee transactions and flag conflicts.
Communication Scan → input text/email snippets, flag suspicious keywords.
Dashboard shows alerts by category.
5. Reporting Module (/reports)
Generate SEBI-ready compliance reports.
Export PDF/CSV.
Status dashboard (Green/Yellow/Red indicators).
6. AI Compliance Assistant (/assistant)
Chatbot answering questions based on SEBI circulars & compliance guidelines (placeholder AI, use dummy Q&A).
Example: “What’s the reporting timeline for suspicious transactions?”
7. Admin Panel (/admin)
View all registered firms & users.
Review surveillance alerts across firms.
Access audit logs of compliance actions.
📡 Backend API Endpoints
Auth
POST /api/auth/register
POST /api/auth/login
GET /api/auth/me
Assessment
POST /api/assessment/submit
GET /api/assessment/history
Surveillance
POST /api/surveillance/trades
POST /api/surveillance/employees
POST /api/surveillance/communications
GET /api/surveillance/alerts
Reports
GET /api/reports/latest
POST /api/reports/export
Admin
GET /api/admin/users
GET /api/admin/logs
⚖️ Compliance Alignment
Logs all user actions in an immutable Audit Trail.
Rate limiting on API endpoints (protect abuse).
Pre-filled SEBI compliance templates for easy reporting.
🎨 UI/UX Guidelines
Clean, professional dashboard with cards and status indicators.
Color coding:
Green = Compliant
Yellow = Needs Attention
Red = High Risk
Simple forms for data entry (CSV upload, text box).
Responsive design (desktop + mobile).
📊 Pricing / SaaS Model
Free tier: basic assessment + limited surveillance.
Pro tier: full monitoring + PDF reporting.
Enterprise: admin panel + AI assistant + integrations.
🧪 Testing
Add Jest + Supertest tests for:
auth (register/login)
surveillance/trades (detect suspicious trades).
✅ Deliverables
Frontend with pages: /, /assessment, /surveillance, /reports, /assistant, /admin.
Backend with REST API & MongoDB models (User, Assessment, SurveillanceAlert, Report, AuditLog).
Auth with JWT.
Dockerfiles + docker-compose.yml for one-click deployment.
Unit tests for auth & surveillance.
📌 Instruction for Poe: Scaffold the app with working routes, models, and UI placeholders. Use dummy compliance checks (simple regex/heuristics) for MVP. Keep code modular and production-ready.
