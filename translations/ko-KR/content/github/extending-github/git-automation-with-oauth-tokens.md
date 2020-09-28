---
title: Git automation with OAuth tokens
redirect_from:
  - /articles/git-over-https-using-oauth-token/
  - /articles/git-over-http-using-oauth-token/
  - /articles/git-automation-with-oauth-tokens
intro: 'You can use OAuth tokens to interact with {{ site.data.variables.product.product_name }} via automated scripts.'
versions:
  free-pro-team: '*'
  enterprise-server: '*'
---

### Step 1: Get an OAuth token

Create a personal access token on your application settings page. For more information, see "[Creating a personal access token](/github/authenticating-to-github/creating-a-personal-access-token)."

{% tip %}

{% if currentVersion == "free-pro-team@latest" %}
**팁:**
- You must verify your email address before you can create a personal access token. For more information, see "[Verifying your email address](/articles/verifying-your-email-address)."
- {{ site.data.reusables.user_settings.review_oauth_tokens_tip }}
{% else %}
**Tip:** {{ site.data.reusables.user_settings.review_oauth_tokens_tip }}
{% endif %}

{% endtip %}

{% if currentVersion == "free-pro-team@latest" %}{{ site.data.reusables.user_settings.removes-personal-access-tokens }}{% endif %}

### Step 2: Clone a repository

{{ site.data.reusables.command_line.providing-token-as-password }}

To avoid these prompts, you can use Git password caching. For information, see "[Caching your GitHub credentials in Git](/github/using-git/caching-your-github-credentials-in-git)."

{% warning %}

**Warning**: Tokens have read/write access and should be treated like passwords. If you enter your token into the clone URL when cloning or adding a remote, Git writes it to your _.git/config_ file in plain text, which is a security risk.

{% endwarning %}

### 더 읽을거리

- "[Authorizing OAuth Apps](/v3/oauth/)"