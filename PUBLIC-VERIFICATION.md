# Verification and limits

23 October 2026. **Experimental native macOS source.** File-fed local transcription and selected persistence/recovery paths have measured evidence. Native microphone/system recording and complete reference fidelity remain unaccepted.

## Clean-export build inputs and local package checks

Earlier Custom source snapshots used input digests `aae4638139564a77ac26934cd04ee83e38fb53f0d2e848ccd06493fc1b23b1a4` and `37c860ff4cfa6e393d018ccc91c70328be408d54101e6c66b5081c01777f5807`; the associated 118 selected tests, local ad-hoc package check, and 14 focused integrity tests apply only to those recorded snapshots. The current package-preservation source at public main `29d54216830c4888e028d8e27bea5f358ea1be3c` records app build-input digest `c268f5e6b3356be8c7509b5027198fbcef72c1c59a31a92efbc92f307012efc3`. The shared-engine pin remains `c3c68bb96387f3ea1a2d13aa6b3213360273e0d46a96ccc9523c819dfafe4cfb`. The root-alias follow-up candidate is described separately below.

## Hosted clean-export CI

The public workflow uses read-only checkout permissions, macOS 26, selected native regression tests, per-edition packaging, and AudioTap tests. [Initial Custom main run](https://github.com/Ghostzy0/pip-meetings/actions/runs/40120729559) tests the preceding app-input digest `37c860ff4cfa6e393d018ccc91c70328be408d54101e6c66b5081c01777f5807`. At the latest check, `baseline-enhanced` and `pip` completed successfully through speech setup, native regressions, packaging, and AudioTap verification; `pip-enhanced` was still running its native regressions. This is not a completed matrix. The in-progress status in that earlier CI report is historical; it is not a status report for the current public main or this root-alias candidate.

Verified host: Apple Silicon arm64, macOS27.0.1, Xcode27.1/Swift6.4. Intended source target is macOS14.2+ with Swift tools6.2+. Intel and other hosts remain unverified. Local packages are **ad-hoc signed, not Developer ID signed or notarised**. A local build does not establish native recording acceptance.

## Network-denied file transcription

The app owner ran each exact executable below with macOS process policy `(deny network*)`, pinned WhisperKit1.1.0 tiny.en resources and a separate synthetic data directory. All four exited0, producing7 ordered timestamped segments and the complete expected normalized text from the13.98-second synthetic two-voice script. Timestamps stayed chronological and within the source audio. No speaker labels were emitted.

| Local package | Exact tested executable SHA256 |
| --- | --- |
| Neutral Core Replica | `736296eefbaf4d3d275308dfdc6b34846f7b6b96311cc8be997ffdd906e32c9f` |
| Neutral Plus | `195ca8960e40560005e28f9499531c72ac8a4e4166989cfc24c29047fbc30efd` |
| Pip Core | `f405f617bb69675fbdc3c9826cccff08436128aea43209f987d27478bced5566` |
| Pip Plus | `0abb46e3d178b0757c9b556ac497460dc90deca250366e4d83440b6ce048826f` |

Fixture SHA256: `a1e4d2ab03c971b10b8b82839eafce0bfa35f0b280266b85e6ed3533507b7a71`. These are local artifact results, not hashes for an asserted downloadable app. Elapsed time ranged roughly1.1–4.7seconds on this shared host; cache state was not controlled. This single scripted fixture is not a broad accuracy, speaker attribution or performance benchmark. Later exported/rebuilt packages need their own receipts.

Pinned speech setup verified28 files totaling80,389,997bytes. Model/tokenizer revisions, hashes and licences are in [local speech setup](docs/LOCAL-SPEECH.md). Setup downloads are explicit; the recorded transcription tests used no network. No model weights are included in source Git.

## Foundation and reference boundaries

The unchanged MIT Meeting Transcriber0.8.1 foundation at `a4f6af6df2674bc4e18097084a128af469823fab` built separately and passed an earlier synthetic LocalVQE echo probe with57dB reduction. That is echo-processing evidence, not native recording or ASR acceptance. Product builds constrain providers, automatic watcher, updater and debug transports; they share one local functional core.

The neutral replica's home → note → bottom transcript drawer follows an observed Granola7.668.2 vendor demo. It uses original/licensed code and system typefaces. Calendar connection, hosted sharing, cloud assistant/enhancement and reliable speaker identity are unavailable; no complete Granola equivalence is claimed. The custom Plus styles add the same local Open actions projection, with filtering/order/reopen regressions.

## Remaining acceptance

- Clean exported repository setup/builds and final downloaded source/artifact recovery.
- Current native note/transcript/decision/action editing, source links, search/export/reopen, archive recovery and Plus interaction.
- Explicit native microphone/system recording, pause/resume/stop and interrupted capture with actual user grants. No such grant or live capture pass is established here.
- Current screenshots, bounded windows, keyboard/focus, light/dark, reduced motion, VoiceOver, long recordings and measured idle resources.

Source, tests, a successful file transcription and a screenshot are distinct evidence. Review transcripts and exports before use; manual notes/actions do not imply AI extraction. Store files and recordings are not encrypted by this app. No production, stable, signed/notarised or complete offline-device acceptance claim follows from these checks.

## Exported fixture scope

This source export excludes Git-ignored local `.wav` and `.aiff` files, including audio fixtures. The selected `scripts/test-native.sh` regression lane does not use those fixture files. Fixture-dependent and opt-in model-quality tests are not thereby accepted. Some guarded tests skip when audio is absent, while structural `QualityFixtureTests` require the excluded WAVs and fail without them. The full upstream test suite has not been claimed as passing from this clean export.

## Root-alias source follow-up candidate (25 October 2026)

The source repair checks a supplied root for symlink/type, creates through that checked spelling, verifies the created directory, and only then stores its canonical URL. It addresses a reproduced first-create `unsafePath` failure caused by a missing root supplied through the `/private/tmp` alias. Child containment, file validation, private modes and atomic writes remain in place. The only code files changed for this repair are `PipMeetingLibrary.swift` and `PipMeetingLibraryTests.swift`.

Internal focused verification on the matching private source patch passed a 30-test library/persistence run, followed by a separate 2-test root-link rerun that overlaps the earlier suite; these are not 32 distinct tests. Results are inherited evidence from the private worktree; the candidate staging clone did not rerun tests. Current hosted build/package results are recorded by the repository’s [verification workflow](https://github.com/Ghostzy0/pip-meetings/actions/workflows/verify.yml). Successful CI is source/package evidence and does not establish GUI or recording acceptance. Its app build-input manifest is `dbc2bdc115ae56b1a88e396f8d881f553326b2584050f3707d66d8d4cef05b5e`; the shared-engine pin remains `c3c68bb96387f3ea1a2d13aa6b3213360273e0d46a96ccc9523c819dfafe4cfb`. `SOURCE-PROVENANCE.json` records the output file manifest digest. `SOURCE-INPUTS.json` is intentionally preserved as the original pre-export source-input record (`471b65bb4ae6e6bc3c602086d5b0460618d0186d217c5857c2cc5cbd5588dd9d`), not rewritten to represent this follow-up.

The limited private native observations below use synthetic notes and fresh temporary data roots. The original first-create process IDs were not sampled. In the separate existing-note reopen runs, the live process identity was verified against the intended frozen app before interaction; temporary data-root paths, process identifiers, exact executable hashes and raw captures remain private.

| Variant | First-create observation | Separate existing-note reopen |
| --- | --- | --- |
| Custom Pip | One synthetic meeting opened in detail on first create; a title and notes were saved. The first-create process ID was not sampled. | In a separate run, the copied existing note opened with its previously saved title and notes after the live process identity was verified against the intended frozen app. No edit was made. |

These are private diagnostic observations, not binary releases and not included here. They support the library source patch but are not a downloadable product claim. The original `SOURCE-INPUTS.json` remains the initial pre-export input record; the shared-engine pin is unchanged. This limited create/reopen evidence does not establish the whole note workflow, export, action behavior, audio capture, permission acceptance, complete parity or accessibility acceptance.
