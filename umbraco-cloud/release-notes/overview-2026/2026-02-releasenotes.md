# February 2026

## Key Takeaways

* **Opt out of automatic patch upgrades** - Allows project admins to opt out of automatic patch upgrades so you can now fully control when your project upgrades.
* **Disable parallel builds** - Disable parallel builds for Umbraco 9+ sites to prevent resource contention.

## Opt out of automatic patch upgrades

It is now possible to opt out of automatic patch upgrades. The default setting for new projects will be on, and the default settings for existing projects will be on. 

{% hint style="warning" %} 
If you have talked to support to have them set up something that ignores your project then that will still be in effect, but if you then go and use these toggles it will overwrite the stored settings.
{% endhint %}

![UI for selecting which upgrades you want to automatically apply](../../.gitbook/assets/automatic-upgrades.png)

## Disable parallel builds

For Umbraco 9+ sites only!

When deploying to Umbraco Cloud, the build step of a deployment could previously utilize all available resources on the underlying infrastructure. This had the side effect that the deployments could end up experiencing resource contention, causing it to complete slowly or fail entirely.

We have now disabled parallel builds, ensuring that a single deployment can no longer consume all available resources. This reduces issues caused by the "noisy neighbor" effect and improves overall deployment reliability.