# Appdome Android Fuse&Sign action

Appdome's Build-2Secure GitHub Action is an out-of-the-box GitHub CI/CD integration, making it easy for mobile developers to automate the build, signing, and certification of security, anti-fraud, and other protections in Android & iOS apps in GitHub CI/CD pipelines. No code and no SDKs are required.

The purpose of Appdome's Build-2Secure Action for GitHub is to streamline and accelerate cyber and anti-fraud delivery in CI/CD pipelines. To do this, the Build-2Secure Action for GitHub automates three important steps in delivering more secure mobile applications to your users fast: (1) building app-level protections into mobile apps, (2) code signing the protected mobile app, and (3) certifying the security of each protected mobile app. The Appdome Build-2Secure Action for GitHub can be used to deliver Certified Secure™ mobile app security, anti-fraud, anti-malware, mobile anti-bot, and other cyber defense updates to mobile apps on the Appdome Cyber Defense Automation Platform. Use this Action for GitHub as a stand-alone DevSecOps integration or in combination with other DevSecOps integrations in your CI/CD pipeline.  


# Usage

See [action.yml](action.yml)

```yaml
# "AUTO_SIGNING" - Android:
steps:
- name: Appdome build-2secure
  uses: Appdome/github_build-2secure@1.0
  with:
    APP_FILE: "# none_protected_application can be pass as path/on/repository OR https://download_link"
    FUSION_SET_ID: "Appdome Fusion Set_Id Android/iOS"
    SIGN_OPTIONS: "SIGN_ON_APPDOME"
    APPDOME_API_TOKEN: ${{secrets.APPDOME_API_KEY}}
    KEYSTORE_FILE: ${{secrets.KEYSTORE}}
    KEYSTORE_PASSWORD: ${{secrets.KEYSTORE_PASSWORD}}
    KEYSTORE_ALIAS: ${{secrets.KEYSTORE_ALIAS}}
    KEYSTORE_KEY_PASSWORD: ${{secrets.KEYSTORE_KEY_PASS}}
