# ********************************************************************************
# Document 09 -- Python Code (Historical Chart Rendering)
# Rev 1.0.0 - Original Issue
# ********************************************************************************
#
# USAGE NOTE: This file is ready to execute as Python code. To run, simply change
# the file extension from .md to .py and execute. No other modifications required.
#
# ********************************************************************************

# -----------------------------------------------------------------------------
# Purpose
# - This document defines the mandatory Python code reference for rendering
#   historical charts within the Log Analysis System.
# - All instructions are procedural; explanatory rationale and examples are
#   centralized in Document 10 -- Read Me.
# - Deviations or omissions invalidate the package.
# -----------------------------------------------------------------------------

# ==============================
# Python Code Template
# ==============================

import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import matplotlib.dates as mdates
from datetime import timedelta

# ==============================
# TEMPLATE PLACEHOLDERS
# ==============================

# Set the start and end dates (update as needed)
start_date = 'YYYY-MM-DD'  # <-- UPDATE START DATE HERE
end_date   = 'YYYY-MM-DD'  # <-- UPDATE END DATE HERE

# Define the bar width in days and half-width for alignment
bar_width  = 0.9
half_width = timedelta(days=bar_width / 2)

# Create the date range
dates = pd.date_range(start=start_date, end=end_date, freq='D')

# Initialize all data points at zero
data = np.zeros(len(dates))

# Define historical non-zero visits
# First-time users: leave this dictionary EMPTY
# Subsequent users: paste the data from the preceding analysis here
visits_data = {
    # Example:
    # 'YYYY-MM-DD': VALUE,
}

# Apply non-zero visits to the data array
for date_str, count in visits_data.items():
    current_date = pd.to_datetime(date_str)
    if current_date in dates:
        idx = dates.get_loc(current_date)
        data[idx] = count

# Create the figure and axes
plt.figure(figsize=(15, 9))

# 1. Create the bar chart for all days in the range
plt.bar(dates, data, width=bar_width, color='darkorange', label='Visits')

# 2. Add a visual indicator (vertical line marker) only at y=0 for dates with 0 units
zero_dates = dates[data == 0]
zero_data  = data[data == 0]
plt.plot(
    zero_dates,
    zero_data,
    marker='|',
    linestyle='None',
    color='black',
    markersize=12,
    markeredgewidth=2,
    label='Zero Unit Indicator'
)

# Set the y-axis limit and ticks (adjust MAX as needed)
plt.ylim(0, 30)
plt.yticks(np.arange(0, 31, 5))

# Maintain X-axis alignment
x_start_limit = dates[0] - half_width
plt.xlim(x_start_limit, dates[-1] + half_width)

# Format the x-axis
plt.gca().xaxis.set_major_formatter(mdates.DateFormatter('%b %d'))
plt.gca().xaxis.set_major_locator(mdates.DayLocator(interval=5))
plt.xticks(rotation=45, ha='right')

# Add labels and title
plt.title('Bar Chart: Visits (All Approved Human Sessions)')
plt.xlabel('Date')
plt.ylabel('Units')

# Add a thin gray line at y=0 for clarity of the axis baseline
plt.axhline(0, color='gray', linestyle='-')

# Add legend
plt.legend()

# Adjust layout
plt.tight_layout()

# Save the plot
plt.savefig('analysis_start_trigger.png')

# Display the plot
plt.show()

# ********************************************************************************
# End of Document 09 -- Python Code (Historical Chart Rendering)
# This file is complete and has not been truncated.
# ********************************************************************************