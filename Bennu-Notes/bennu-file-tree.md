# Bennu — Project File Tree

```
Bennu/
├── Bennu.xcodeproj
├── README.md
├── CONTRIBUTING.md
├── LICENSE                          # GPLv3
│
├── App/
│   ├── BennuApp.swift               # @main entry point
│   ├── AppDelegate.swift            # (if needed for lifecycle/notifications)
│   └── AppEnvironment.swift         # shared environment/config objects
│
├── DesignSystem/
│   ├── Colors.swift
│   ├── Typography.swift
│   ├── Icons.swift
│   ├── Theme.swift                  # calm/clinical-but-warm system
│   └── Components/
│       ├── PrimaryButton.swift
│       ├── TagChip.swift
│       ├── CalendarDayCell.swift
│       └── ConfidenceBadge.swift    # used in Phase 3 predictions
│
├── Models/
│   ├── Cycle.swift
│   ├── Period.swift
│   ├── Symptom.swift
│   ├── Mood.swift
│   ├── CustomField.swift
│   ├── CustomTag.swift              # Phase 2
│   └── Note.swift
│
├── Persistence/
│   ├── SwiftDataStack.swift         # or CoreDataStack.swift
│   ├── Encryption/
│   │   └── AtRestEncryption.swift
│   ├── Migrations/
│   └── Repositories/
│       ├── CycleRepository.swift
│       ├── SymptomRepository.swift
│       └── SettingsRepository.swift
│
├── Onboarding/
│   ├── OnboardingFlowView.swift
│   ├── Steps/
│   │   ├── WelcomeStepView.swift
│   │   ├── LastPeriodStepView.swift
│   │   ├── AverageCycleLengthStepView.swift
│   │   └── GoalsStepView.swift
│   └── OnboardingViewModel.swift
│
├── Tracking/                        # Phase 1 core tracking
│   ├── Calendar/
│   │   ├── CalendarView.swift
│   │   └── CalendarViewModel.swift
│   ├── LogPeriod/
│   │   ├── LogPeriodView.swift
│   │   └── LogPeriodViewModel.swift
│   ├── LogSymptomsMood/
│   │   ├── LogSymptomsView.swift
│   │   ├── LogMoodView.swift
│   │   └── LogEntryViewModel.swift
│   └── QuickLog/
│       └── QuickLogWidgetView.swift # quick-log mode, Phase 2
│
├── Customization/                   # Phase 2
│   ├── CustomTagsView.swift
│   ├── TrackingCategoriesEditorView.swift
│   ├── WorkflowModeSettingsView.swift  # quick vs detailed
│   ├── RemindersSettingsView.swift
│   └── NotificationsScheduler.swift
│
├── Insights/                        # Phase 3
│   ├── TrendsView.swift
│   ├── CorrelationsView.swift
│   ├── PredictionEngine/
│   │   ├── CyclePredictor.swift
│   │   ├── FertileWindowPredictor.swift
│   │   └── ConfidenceCalculator.swift
│   └── HistoryBrowserView.swift
│
├── DataPortability/                 # Phase 4
│   ├── Export/
│   │   ├── PDFExporter.swift
│   │   ├── CSVExporter.swift
│   │   └── ExportOptionsView.swift
│   ├── BackupRestore/
│   │   ├── EncryptedBackupManager.swift
│   │   ├── ICloudOptionalSync.swift
│   │   └── RestoreFlowView.swift
│   └── Privacy/
│       ├── PrivacyExplainerView.swift
│       └── AppLockManager.swift      # Face ID / Touch ID
│
├── Settings/
│   ├── SettingsView.swift
│   ├── AppearanceSettingsView.swift  # dark mode toggle
│   └── AboutView.swift
│
├── Accessibility/                    # Phase 5
│   ├── DynamicTypeModifiers.swift
│   └── VoiceOverLabels.swift
│
├── Localization/                     # Phase 5 scaffolding
│   ├── en.lproj/
│   │   └── Localizable.strings
│   └── LocalizationHelper.swift
│
├── SharedUI/
│   ├── EmptyStateView.swift
│   ├── ErrorStateView.swift
│   └── LoadingView.swift
│
├── iPad/                             # Phase 5 iPad-specific layout
│   ├── SplitViewContainer.swift
│   └── SidebarView.swift
│
├── Resources/
│   ├── Assets.xcassets
│   ├── Presets/
│   │   ├── DefaultSymptoms.json
│   │   └── DefaultMoods.json
│   └── Fonts/
│
├── BennuTests/
│   ├── Models/
│   ├── PredictionEngineTests/
│   ├── PersistenceTests/
│   └── ExportTests/
│
├── BennuUITests/
│   ├── OnboardingUITests.swift
│   ├── TrackingUITests.swift
│   └── AccessibilityUITests.swift
│
└── .github/
    └── workflows/
        └── ci.yml                   # build/lint/test on push
```
