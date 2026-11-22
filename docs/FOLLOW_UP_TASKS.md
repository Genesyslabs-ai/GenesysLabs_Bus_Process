# Follow-up tasks after V0.3 baseline integration

These are proposed tasks, not approved changes or business policies. The integration preserves the original application and workflow data.

1. **Business validation:** walk an infrastructure deal and a KeyValue-only software deal through the model with Joice, Jecko and Arshad. Review combined/consulting paths, both shipment choices and unresolved contractual/payment checkpoints.
2. **Decision and exception modeling:** represent rejection, no-go, cancellation, rework, failed acceptance and escalation as explicit connections. The current lifecycle and subprocess diagrams are predominantly sequential; narrative questions do not establish executable branches.
3. **View consistency:** route labels, responsibility lanes and contracts/logistics diagrams contain hardcoded text separate from editable stage data. Propose a compatible shared representation before making these views fully editable.
4. **Review states and provenance:** propose `needs_review`, reviewer/date and decision references without silently changing the existing three-status model or exported data.
5. **Import validation:** validate all fields used by renderers, unique/expected IDs and nonempty subprocesses. The current importer checks only a small subset of the record structure. Any strengthening needs compatibility fixtures, including a real historical V0.2 export.
6. **Workshop UX:** separately review laptop readability, inspector behavior, focus-mode navigation and keyboard access. No redesign is included in this milestone.
7. **Brand consistency:** review legacy UI uses of `GenesysLabs` against the canonical `GenesysLabs.ai` spelling as a separate approved UI/content change.
8. **Optional infrastructure learning:** review Docker port binding, then consider Git review practices, CI and authenticated hosting when useful. None is required for the static app baseline.

Keep payment recipients, consulting fee credits, KeyValue contracts, importer responsibilities, warranty and legal structures open until the appropriate owners confirm them. Record future approved business changes in the operating specification and decision log together with app changes.
