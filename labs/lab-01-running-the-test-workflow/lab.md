# Running the Test Workflow

## Time Required

20 minutes

## Overview

In this lab, you will execute a sample test workflow, review core pipeline architecture components, run verification checks, and validate execution results.

### You learn how to:
- Prepare and configure your test workflow environment.
- Execute automated verification checks using command-line tools.
- Inspect execution logs and artifacts for structural correctness.
- Validate pipeline integrity against expected outcomes.

## Scenario

Your team is adopting a structured test pipeline to ensure consistent code quality and prevent regressions. In this lab, you practice running the end-to-end verification workflow, inspecting logs, and confirming that all checks pass successfully.

## Lab Instructions

### Task 1: Prepare your environment

In this task, you set up your working environment and verify access to the pipeline tools and scripts.

1. Open your terminal or Cloud Shell environment.

2. Navigate to the course repository root directory:

```bash
cd test-course
```

3. Confirm that the test scripts directory exists and is accessible:

```bash
ls -la scripts/
```

> [!NOTE]
> You should see the automated check scripts and helper utilities listed in the directory output.

<!-- TODO IMAGE: Terminal view of scripts directory contents -->
![Scripts directory listing](images/scripts-listing.png)

### Task 2: Run verification checks

In this task, you execute the test workflow script with strict verification enabled.

1. Run the test workflow check script with strict mode and reporting enabled:

```bash
./scripts/run-checks.sh --strict --report
```

2. Review the console output to observe each execution stage and validation check.

> [!IMPORTANT]
> Ensure all individual check stages report success before proceeding to artifact inspection.

### Task 3: Inspect execution logs and artifacts

In this task, you examine the generated logs and artifacts to confirm structural correctness and adherence to acceptance criteria.

1. List the generated report and log artifacts:

```bash
ls -la reports/
```

2. View the summary of the latest test run:

```bash
cat reports/latest-run.log
```

> [!TIP]
> Inspecting logs immediately after a run helps surface subtle warnings before they become production regressions.

## Bonus Task 4: Simulate and troubleshoot a failure

In this optional task, you observe how the pipeline handles errors and practices troubleshooting.

1. Temporarily modify a test configuration or run a dry-run check with invalid parameters to trigger a controlled failure.

2. Observe how the fail-fast principle surfaces the error message and pinpoints the exact regression point.

3. Restore your configuration and rerun the checks to confirm recovery.

## Congratulations!

In this lab, you have:
- Prepared and configured your test workflow environment.
- Executed automated verification checks using command-line tools.
- Inspected execution logs and artifacts for structural correctness.
- Validated pipeline integrity against expected outcomes.
