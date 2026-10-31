# Achuth portfolio starter

A responsive static website for GitHub Pages. Open `index.html` in a desktop browser to review it. No installation, account, build tools, or paid hosting service is needed for local preview.

This draft contains nine labeled image placeholders. Descriptions are draft copy based on the project brief. Review them and add your actual contact information and professional links before sharing broadly. No performance measurements or medical validation are claimed.

## Publish on GitHub Pages

1. Create a public GitHub repository named YOUR-USERNAME.github.io, replacing YOUR-USERNAME with your actual GitHub username.
2. Extract this ZIP. Upload the contents of the achuth-portfolio folder to the repository root. `index.html` must be at the root, not inside an additional folder. Include the assets folder. Include .nojekyll if your file picker displays it; this plain HTML site also works without it.
3. Commit the uploaded files to main.
4. In the repository, open Settings > Pages. Select Deploy from a branch, choose main and /(root), and save.
5. Wait for deployment and visit https://YOUR-USERNAME.github.io. The live website and the files in a public repository are public.

## Connect Achuth.co

First, verify domain ownership in your GitHub account Settings > Pages. Use Add a domain, enter achuth.co, and add the exact TXT record GitHub provides at your DNS provider. Keep that verification record.

After verification, open the repository Settings > Pages and set Custom domain to achuth.co. GitHub creates a CNAME file when publishing from a branch; retain this file in future uploads.

If using Namecheap BasicDNS, PremiumDNS or FreeDNS, open Domain List > Manage next to achuth.co > Advanced DNS > Host Records. If the domain uses other nameservers, edit DNS with that provider instead.

Add these records (TTL Automatic is fine):

| Type | Host | Value |
| --- | --- | --- |
| A | @ | 185.199.108.153 |
| A | @ | 185.199.109.153 |
| A | @ | 185.199.110.153 |
| A | @ | 185.199.111.153 |
| CNAME | www | YOUR-USERNAME.github.io |

Replace YOUR-USERNAME with your actual GitHub username. Do not include https:// or a repository path in the CNAME value. Replace conflicting parking or redirect records for @ or www. Preserve unrelated email/MX records and the GitHub verification TXT record. Remove conflicting old A/AAAA records for these website hosts if present. Do not add a wildcard record.

Allow DNS time to update, potentially up to 24 hours. In GitHub Pages, enable Enforce HTTPS once the certificate is available. Test https://achuth.co and https://www.achuth.co. GitHub redirects www to the configured apex domain when both are set up correctly.

GitHub Pages for a public repository is available on GitHub Free. Your domain renewal is a separate recurring expense.

Official setup references, checked October 29, 2026:
- https://docs.github.com/en/pages/quickstart
- https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site
- https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/verifying-your-custom-domain-for-github-pages
- https://www.namecheap.com/support/knowledgebase/article.aspx/9645/2208/how-do-i-link-my-domain-to-github-pages/

## Add the planned images

Place files in assets/images with these exact lowercase names:

| Project | Image filenames |
| --- | --- |
| Robotic hand | hand-cad.jpg, hand-assembled.jpg, hand-demo.jpg |
| Cardiovascular simulation | cardio-architecture.jpg, cardio-output-1.jpg, cardio-output-2.jpg |
| Holter monitor | holter-system.jpg, holter-assembly.jpg, holter-output.jpg |

If your source uses PNG or WebP, update the corresponding data-src extension in index.html. The page displays images without cropping. Click an uploaded image to enlarge it. The Escape key closes the image viewer.

Export clear web copies and retain your originals separately. For photographs, try around 1600-2000 pixels on the long edge and JPEG/WebP compression. For graphs and diagrams, PNG often preserves labels well. Check readability on a phone. Remove personal identifying data from ECG screenshots.

Each image has a visible caption and an alt attribute in index.html. Update both to describe the actual content. Graph captions should name the simulated or measured condition and explain what the reader should notice.

## Add more photos or expand a project

Copy an existing figure element within the relevant project section, change its data-src path, alt text, title, and caption, and upload the new image. Images can be added to an existing gallery-pair container, or create another gallery-pair for a new row. Keep the primary image as an overview.

Project text lives directly in index.html. The three sections have the IDs robotic-hand, cardiovascular, and holter. The CSS is inside style tags and the small image-viewer script is at the end. All site code is contained in this file, so it is easy to move to a different host later.

The Documentation to develop expandable area in each project identifies useful follow-up content. Replace it with real methods, findings, and limitations as the case studies mature. The image slots are placeholders, not measured results.

To add your resume, upload a public-safe PDF such as assets/achuth-resume.pdf and add a link to it in the About section. Add your real email with a mailto link and your real GitHub/LinkedIn URLs in the contact section. No invented account links are included.

## Before sharing broadly

Check contact links, image captions, mobile layout, graph units, and the accuracy of each project description. Confirm which project materials you have permission to publish. A public GitHub repository makes uploaded source files and their history publicly accessible.

Files attached to a ChatGPT project do not automatically update GitHub Pages. Revised website files and images must be committed to the GitHub repository to update the live site.
