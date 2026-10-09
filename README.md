SCHOLARAI“Fund Your Education. Learn. Intern. Build. Grow.”An AI-powered 3D spatial ecosystem connecting students, universities, government bodies, foundations, and enterprises for scholarships, education funding, internships, and career progression.OverviewScholarAI merges a WebGL 3D interface with deterministic matching and financial ledger clarity. It moves away from flat dashboards into an interactive spatial universe built on Three.js, offering clear visualizations for funding pipelines, fee distribution, career graphs, and internship training.The core journey follows a unified lifecycle:$$\text{FUND} \longrightarrow \text{LEARN} \longrightarrow \text{INTERN} \longrightarrow \text{BUILD} \longrightarrow \text{CERTIFY} \longrightarrow \text{CAREER}$$Key Features1. Spatial 3D Universe (Three.js & WebGL)Smooth Camera Navigation (flyCameraTo): Smooth coordinate and vector interpolation transitions between stations:Sector 0: Universe Core (Hero)Sector 1: Funding UniverseSector 2: AI Neural Core & MatcherSector 3: 3D Career Progression GraphSector 4: Internship Learning LabSector 5: College Command & Fee LedgerInteractive Geometry: Ambient floating icosahedrons, animated torus knots, dual-ring gyroscopic AI cores, and dynamic raycasting.Responsive Performance: Automatic particle scaling and adaptive device-pixel-ratio handling.2. Deterministic AI Matching EngineRule Constraint Engine: Replaces unpredictable LLM hallucinations with deterministic calculations:Academic Validation: Strict threshold checks against GPA/CGPA requirements.Socioeconomic Constraints: Annual family income limits verified in INR (₹).Discipline Mapping: Targeted matching based on major and specialization.Document Completeness: Flags missing documentation (e.g., current FY Income Certificates) before submission.Live Match Score Breakdown: Real-time percentage scoring with itemized pass/fail criteria.3. Integrated AI Career CopilotPersistent floating drawer offering instant answers for:Application eligibility queries.Missing prerequisite document checks.12-week internship syllabus breakdowns.Role-based administrative summaries.4. College Fee Protection & 3D LedgerAccounting Protection: Prevents premature deductions; distinguishes between Awarded, Committed, and Credited funds.Interactive Visual Formula:$$\text{Remaining Due (₹70,000)} = \text{Annual Fee (₹1,20,000)} - \text{Committed Scholarship (₹50,000)}$$Real-time circular SVG gauges and departmental rosters with CSV bulk import simulation.5. 12-Week Internship Lab & Mentor EvaluationWeek-by-week curriculum tracking from foundational architecture to production releases.Code submission workspace with an integrated rubric evaluation engine:Technical SkillsCode Hygiene & ModularityDocumentation QualityProblem Solving & Efficiency6. Role-Based Access Control (RBAC)Seamless perspective switching between Student, College Admin, Organization/Enterprise, and Super Admin.Architecture & Technology StackScholarAI/
├── Frontend Core
│   ├── Three.js (r128 via CDN)       # WebGL 3D rendering pipeline
│   ├── Vanilla JS (ES6+)             # Deterministic logic, state management, and camera physics
│   ├── Tailwind CSS (via CDN)        # Glassmorphism, typography, and responsive layouts
│   └── Lucide Icons                  # Clean visual iconography
└── Architecture Specification
    ├── Client State Engine           # Synchronizes 3D spatial coordinates with UI HUD overlays
    ├── Deterministic Matcher         # JSON-logic constraint solver for funding eligibility
    └── Event-Driven Event Bus        # Handles multi-portal role switching and form submissions
Getting StartedPrerequisitesAny modern web browser supporting WebGL (Chrome, Edge, Firefox, Safari).A lightweight static file server (VS Code Live Server, Python http.server, or Node-based serve).Installation & Local RunClone or Download the Repository:Bashgit clone https://github.com/your-username/scholarai.git
cd scholarai
Serve the Application:Using Python:Bashpython -m http.server 8080
Using Node.js:Bashnpx serve .
Launch in Browser:Navigate to http://localhost:8080/index.html.Database Schema (Production Blueprint)       ┌──────────────────────┐
       │      User (Auth)     │
       │  (Role, MFA, Audit)  │
       └──────────┬───────────┘
                  │ 1:1
       ┌──────────┴───────────┐
       │   Student Profile    │
       │ (Academic, KYC, EWS) │
       └────┬───────────────┬─┘
            │               │
     1:M    │               │ 1:M
┌───────────▼─────┐   ┌─────▼─────────────┐
│  Applications   │   │  Career Graph     │
│ (State Machine) │   │ (Nodes & Progress)│
└─────┬───────────┘   └───────────────────┘
      │ M:1
┌─────▼─────────────────────────┐
│ Opportunity / Funding Program │
│ (Govt, Corporate, Trust, NGO) │
└─────▲─────────────────────────┘
      │ M:1
┌─────┴─────────────────────────┐
│     Organization / College    │
│  (Verified Status, Escrow)    │
└───────────────────────────────┘
Security & Verification StandardsAudit Logs: Immutable tracking for program updates, document approvals, and ledger settlements.Escrow Separation: Corporate and philanthropic endowments remain in verification states until clearing confirmations match regulatory guidelines.Client-Side Graceful Degradation: Fallbacks to simplified canvas rendering and smooth scrolling if WebGL context creation fails on lower-powered devices.
