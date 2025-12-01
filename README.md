# NextStrain Community Analysis Repository

This repository is a central place to share and view Nextstrain phylogenetic analyses. It uses the [nextstrain.org community sharing feature](https://docs.nextstrain.org/en/latest/guides/share/community-builds.html), which automatically serves datasets stored in this GitHub repository.

## How It Works

The `nextstrain.org` platform is configured to monitor this repository. Any correctly formatted dataset files (`.json`) placed in the `auspice/` directory on the `main` branch will automatically become available for viewing online.

The key is to follow a specific file naming convention, which determines the final URL for your dataset.

---

## How to Contribute a New Dataset

To add your own analysis results, please follow these steps.

### 1. Prepare Your Dataset File

After running your Nextstrain analysis, you will have an output JSON file located in the `auspice/` directory of your build. This is the file you need to share (e.g., `zika.json`).

### 2. Rename Your File Correctly

This is the most important step. The filename **must** follow this format:

`repository-name_part1_part2_..._partN.json`

*   **`repository-name`**: This must be the literal name of this repository, which is **`nextstrain-share`**.
*   **`_part1_part2_...`**: These are underscore-separated names that describe your dataset. They will be converted into slash-separated parts in the final URL.

**Example:**
If you have an analysis of Dengue Serotype 3, a good filename would be:
`nextstrain-share_dengue_serotype-3.json`

### 3. Add the File to the Repository

Place your correctly named JSON file inside the `auspice/` directory in this repository.

### 4. Submit Your Changes

If you have write access to this repo, you can commit the file directly. Otherwise, the best way to contribute is by opening a Pull Request:
1.  **Fork** this repository.
2.  **Clone** your fork to your local machine.
3.  Create a **new branch** for your dataset (e.g., `git checkout -b add-dengue-dataset`).
4.  Add your file to the `auspice/` folder.
5.  **Commit** and **push** your changes to your fork.
6.  Open a **Pull Request** from your fork to this repository's `main` branch.

---

## Viewing Datasets

Once a dataset is merged into the `main` branch, it may take 5-10 minutes for it to become available on nextstrain.org due to caching.

The URL structure is:
`https://nextstrain.org/community/<USERNAME>/<REPO-NAME>@main/<PART1>/<PART2>`

### Example links

| File in `auspice/` directory                | Resulting Nextstrain URL                                                               |
| ------------------------------------------- | -------------------------------------------------------------------------------------- |
| `nextstrain-share_mpox-analysis.json`       | [nextstrain.org/community/LucvZon/nextstrain-share@main/mpox-analysis](https://nextstrain.org/community/LucvZon/nextstrain-share@main/mpox-analysis)                               |
| `nextstrain-share_zika.json`               | [nextstrain.org/community/LucvZon/nextstrain-share@main/zika](https://nextstrain.org/community/LucvZon/nextstrain-share@main/zika)                             |
| *`nextstrain-share_dengue_serotype-3.json`* | *`.../nextstrain-share@main/dengue/serotype-3`* (Hypothetical example)                  |

To see a list of all available datasets, visit the base community URL:
[https://nextstrain.org/community/LucvZon/nextstrain-share@main](https://nextstrain.org/community/LucvZon/nextstrain-share@main)

### Sharing Narratives

The process is similar for sharing [Nextstrain Narratives](https://docs.nextstrain.org/en/latest/tutorials/narratives-how-to-write.html).
*   Place your markdown file (`.md`) in the `narratives/` directory.
*   Follow the same file naming convention (`nextstrain-share_my-narrative.md`).
*   The URL will be accessible under `/narratives/`.
