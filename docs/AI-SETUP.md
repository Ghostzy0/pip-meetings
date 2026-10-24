# Set up Pip Meetings

This custom repository contains Neutral Plus, Pip Core and Pip Plus; Pip Core is the default. Follow the README for platform requirements and use only the editions listed in `distribution.json`.

```sh
scripts/test-native.sh pip
scripts/build-native.sh pip
scripts/test-native.sh baseline-enhanced
scripts/build-native.sh baseline-enhanced
scripts/test-native.sh pip-enhanced
scripts/build-native.sh pip-enhanced
python3 scripts/setup-speech.py
python3 scripts/setup-speech.py --verify-only
open 'dist/pip/Pip Meetings.app'
```

Initial builds and speech setup download pinned public dependencies and the explicitly documented local model files. Consult [public verification](../PUBLIC-VERIFICATION.md) for tested network and package evidence. Processing stays local after setup only for paths covered by those checks. Native recording requires the user's actual macOS permissions and participant consent; never bypass consent or upload meeting content.
