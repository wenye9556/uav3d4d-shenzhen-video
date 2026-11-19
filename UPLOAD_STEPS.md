# Upload steps (run in your own GitHub account)

The upload is prepared locally but **not pushed**. The folder contains the
English v11 MP4, the delivery manifest, and this README (the Chinese narration
copy is retained offline by the authors).

## 1. Create the empty repository

On GitHub, create a public repository named:

`uav3d4d-shenzhen-video`

Do **not** initialize it with a README, .gitignore, or license. Copy the
repository URL.

## 2. Initialize and push from this folder

```powershell
cd E:\无人机3D\code\REVISION_TRE_D_26_04139\04_supplement\video\github_upload
git init
git add .
git commit -m "Add v11 60-second English Shenzhen UAV case video"
git branch -M main
git remote add origin https://github.com/<YOUR_GITHUB_ACCOUNT>/uav3d4d-shenzhen-video.git
git push -u origin main
```

Replace `<YOUR_GITHUB_ACCOUNT>` with your account name.

## 3. Verify the upload

```powershell
Get-FileHash .\uav3d4d_sz_60s_en.mp4 -Algorithm SHA256
Get-FileHash .\uav3d4d_sz_60s_zh.mp4 -Algorithm SHA256
```

Compare against `uav3d4d_sz_60s_delivery_manifest.json`.

## 4. Public URL

After the push, the repository URL is:

`https://github.com/<YOUR_GITHUB_ACCOUNT>/uav3d4d-shenzhen-video`

Use that URL in the manuscript/reply letter. Do not substitute a temporary
local path. If a DOI snapshot is needed later, archive the same folder on
Zenodo.

## Boundary

- Do not upload the manuscript source, experiment records, or internal audit
  files to this public repository.
- Keep the two MP4 files, the manifest, and this README as the public package.
- The video is a supplement; it does not replace the paper or the frozen
  experiment records.