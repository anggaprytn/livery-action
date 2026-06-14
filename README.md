# Livery Action

Private-alpha GitHub Action bundle for deterministic Livery brand checks.

Use the public distribution repo:

```yaml
- uses: anggaprytn/livery-action@v0.1.0-rc.6
  with:
    brand_id: brand_livery_test
    api_url: ${{ secrets.LIVERY_API_URL }}
    api_key: ${{ secrets.LIVERY_API_KEY }}
    mode: changed
    fail_on: high
    upload: true
```

Required files in the distribution repo:

- `action.yml`
- `dist/index.cjs`
- `README.md`

The main Livery source repo can remain private. Consumer repos only need `LIVERY_API_URL` and `LIVERY_API_KEY` when this bundle is published and tagged.
