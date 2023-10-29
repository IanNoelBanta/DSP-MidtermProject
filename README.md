# DSP-MidtermProject

Mema steps:
1. collection 
2. descriptive stats - to understand the data's distribution and structure (dito na ata yung part na gagamiting yung stats, mean median mode shts, standard deviation shts, minimum at maximum value)
3. visualization (galing don sa previous sht ^)
4. dsp (fourier analysis daw eh sabi ni bff para maidentify any dominant frequencies in the data). marreveal daw neto yung daily, weekly, or other cyclic patterns <- kailangan din toh diba
    - dito rin ata magffilter, digital filters daw to remove noise or isolate specific frequency components, if necessary. yung pag remove ng noise nasa part na ata ng stats, marremove na ata agad.
5. time series analysis - mag time series decomposition daw para maseparate yung data into trend, seasonality, and shts
6. numerical methods - implement regression analysis para mamodel yung relationship between temp and humi or to predict one based on the other. apply daw ng smoothing techniques like moving avarages or exponential smoothing to reduce noice and highlight trends.
7. hypothesis testing - so dapat may ata may hypothesis tayo? HAHAHAH. use statistical hypothesis tests daw to determine if there are significant differences between different time periods. tas perform statistical tests to assess correlations or casual relationships between temp and humi and other variables, such as time of day or external factors.
8. anomaly detection - di ko sure kung kailangan pa ba talaga toh pero sabi identify anomalies or unusual patterns in the data that may indicate equipment malfunctions, sensor errors, or extreme weather events.
9. machine learning - shesh mlp lezgo. apply machine learning techniques like clustering or time series forecasting to further explore and predict temperature and humidity patterns.
10. data interpretation - summarize your findings and draw conclusions about the data. communicate any insights, trends, or anomalies in a clear and concise manner.


------------------------------------------------------------------------------------------------------------------------------------------------
------------------------------------------------------------------------------------------------------------------------------------------------
------------------------------------------------------------------------------------------------------------------------------------------------

Specifically, the project should answer the following questions: 
1. What is the periodicity of the data? 

WHAT??

The periodicity of data refers to the presence of recurring patterns or cycles at regular intervals within the data. In other words, it signifies that the data exhibits a predictable and repetitive behavior over time. Periodic data can be found in various fields, including finance, economics, meteorology, and many others.

Key characteristics of periodic data include:

1. **Regular Intervals:** Periodic data displays patterns or cycles that occur at consistent time intervals. For example, daily temperature data often exhibits a 24-hour periodicity with daytime highs and nighttime lows.

2. **Predictability:** Periodic data allows you to make predictions about future values based on the observed patterns. If you identify a recurring cycle, you can anticipate when certain events or conditions are likely to repeat.

3. **Seasonality:** Seasonal patterns are a common form of periodicity. For instance, retail sales tend to spike during holiday seasons every year, demonstrating an annual periodicity.

4. **Frequency:** The frequency of a periodic pattern refers to how often it repeats within a given time frame. For example, monthly sales data has a frequency of one cycle per month.

5. **Amplitude and Phase:** Periodic data often exhibits variations in amplitude (the range of values within a cycle) and phase (the timing or alignment of the cycle).

6. **Waveform Analysis:** Periodic data can often be described using waveform functions, such as sine or cosine waves, to model the underlying patterns.

Understanding the periodicity of data is crucial for various applications, including:

- **Forecasting:** Identifying and characterizing periodic patterns helps in making predictions about future data points, especially in time series analysis.

- **Anomaly Detection:** Detecting deviations from expected periodic patterns can help in identifying unusual events or outliers.

- **Resource Allocation:** Businesses and organizations can use knowledge of periodic patterns to allocate resources effectively, such as staffing during peak demand times.

- **Optimization:** Periodic data can inform decisions on scheduling, inventory management, and maintenance activities.

Analyzing periodic data may involve using techniques like Fourier analysis, spectral analysis, or time series modeling to extract and quantify the periodic components. Understanding the periodicity of data can lead to more informed decision-making and improved modeling of systems with cyclical behaviors.


HOW??

Analyzing the periodicity of collected temperature and humidity data involves identifying and characterizing recurring patterns in the data. To do this, you can follow these steps:

1. **Data Collection and Preparation:**
   - Ensure you have collected and organized your temperature and humidity data with timestamps.

2. **Data Cleaning:**
   - Clean the data to handle missing values, outliers, and inconsistencies. This is a crucial step to ensure the data's quality.

3. **Time Series Plot:**
   - Create a time series plot to visualize the entire dataset. This can help you identify any visible patterns or trends.

4. **Resampling:**
   - Depending on the frequency of your data (e.g., hourly, daily), you may need to resample the data to a consistent time interval to ensure uniformity in your analysis.

5. **Periodogram Analysis:**
   - Compute a periodogram, which is a graphical representation of the frequency components in the data. It helps identify dominant periodicities. You can use techniques like the Fast Fourier Transform (FFT) to calculate the periodogram.

6. **Peak Detection:**
   - Identify the peaks in the periodogram. These peaks correspond to the dominant periodic frequencies in your data.

7. **Waveform Analysis:**
   - For each dominant periodicity identified, fit a sinusoidal wave (e.g., sine or cosine function) to the data to describe the periodic pattern. Determine the amplitude, phase, and frequency of the wave.

8. **Visualization:**
   - Plot the fitted sinusoidal waves on top of the original data to visualize how well they capture the periodic patterns.

9. **Statistical Analysis:**
   - Use statistical tests to assess the significance of the periodic patterns. You can conduct hypothesis tests to determine if the periodicity is statistically significant.

10. **Modeling:**
    - Depending on the complexity of the periodic patterns, you may consider time series modeling techniques like seasonal decomposition (e.g., STL decomposition) to separate the data into trend, seasonal, and residual components.

11. **Further Analysis:**
    - If there are multiple periodic patterns (e.g., daily and weekly), analyze each separately and examine how they interact.

12. **Interpretation:**
    - Interpret the results in the context of your analysis goals. For example, if you are analyzing temperature and humidity data, you might identify daily temperature variations and weekly humidity patterns.

13. **Usefulness:**
    - Consider how the knowledge of periodicity can be used for various applications, such as weather forecasting, energy management, or resource allocation.

14. **Reporting:**
    - Document your analysis process, findings, and any actions or decisions based on the identified periodicity.

15. **Further Research:**
    - If you want to explore the data further, you can investigate the relationships between periodicity and external factors (e.g., weather events, seasonality) that may influence the observed patterns.

The choice of tools and techniques for periodicity analysis may depend on the complexity of the data and your expertise. Common tools for this type of analysis include Python with libraries like NumPy, pandas, Matplotlib, and SciPy for signal processing, or specialized time series analysis software packages like R or MATLAB.



2. What are the central tendencies of the data according to time of day, day of week, and in general? 

WHAT??

Central tendencies, which include measures like mean, median, and mode, can provide valuable insights when analyzing data according to time of day, day of the week, and in general. Here's what these central tendencies mean in each context:

**1. Time of Day:**

- **Mean:** The mean (average) value for a specific time of day provides information about the typical or expected value of the data at that time. For example, if you calculate the mean temperature at 2:00 PM over a two-week period, it tells you the average temperature for that time.

- **Median:** The median at a specific time of day represents the middle value when the data is ordered. It can help identify the typical or central value that is not skewed by extreme outliers.

- **Mode:** The mode at a particular time of day is the most frequently occurring value. It can reveal the most common conditions or situations at that time.

**2. Day of the Week:**

- **Mean:** Calculating the mean for a specific day of the week provides insight into the average value for that particular day. For example, the mean temperature on Sundays over two weeks helps identify the typical Sunday temperature.

- **Median:** The median on a specific day of the week helps identify the middle value for that day, which can be useful for understanding what's typical without being influenced by outliers.

- **Mode:** The mode for a particular day of the week indicates the most common value, which can be related to recurring patterns or events on that day.

**3. In General (Overall):**

- **Mean:** When calculating the overall mean, it provides a measure of central tendency for the entire dataset. It represents the average value across all time periods, days of the week, or whatever time intervals the data covers.

- **Median:** The overall median identifies the middle value of the entire dataset, which can be useful for understanding the central tendency of the data without being significantly influenced by extreme values.

- **Mode:** The overall mode is the most frequently occurring value in the entire dataset. It highlights the most common conditions or situations in the data.

Central tendencies are important for summarizing and understanding data across different time intervals, as they provide a way to describe what's typical, average, or most common. These statistics can be particularly useful when analyzing time-series data, such as temperature and humidity, as they help uncover patterns, trends, and variations over time or within specific time segments.


HOW?? 

Performing data analysis for collected data, especially when focusing on central tendencies at different time intervals, involves several steps. Here's a general process to follow:

1. **Data Collection:**
   Collect and organize your temperature and humidity data. Ensure that the data is timestamped, indicating the time and date of each measurement.

2. **Data Cleaning:**
   Before analysis, clean the data to handle missing values, outliers, and inconsistencies. This step is crucial to ensure the data's quality.

3. **Time Segmentation:**
   Depending on your analysis goals, segment the data into the relevant time intervals. This can include time of day (e.g., hourly), day of the week, or specific date ranges.

4. **Calculate Central Tendencies:**
   For each time interval or segment, calculate the central tendencies you're interested in:

   - **Mean:** Sum all values in the interval and divide by the number of data points.
   - **Median:** Arrange the data points in ascending order and find the middle value.
   - **Mode:** Identify the most frequently occurring value in the interval.

5. **Visualize the Data:**
   Create plots and graphs to visualize the central tendencies over time. Line plots, bar charts, and histograms can help you see trends and variations.

6. **Statistical Analysis:**
   Perform statistical tests to determine the significance of central tendency differences between time intervals or days of the week. For example, you can use t-tests or ANOVA to compare means.

7. **Interpret the Results:**
   Analyze the central tendencies and statistical results to draw conclusions. Determine whether there are any patterns or significant differences between time intervals or days.

8. **Inferential Analysis:**
   Depending on your data, you may want to make inferences or predictions. Time series forecasting, regression analysis, or other modeling techniques can be used for this purpose.

9. **Report and Visualization:**
   Present your findings in a clear and understandable way. Use visualizations, tables, and written explanations to communicate your results effectively.

10. **Consider Additional Factors:**
    While central tendencies are important, consider other factors that may influence the data, such as external events (e.g., holidays, weather events) or seasonal variations.

11. **Repeat as Needed:**
    If your analysis requires deeper investigation or comparison over longer periods, repeat the process with different time intervals or subsets of the data.

12. **Document Your Methodology:**
    Keep detailed records of your data cleaning, analysis steps, and the tools and techniques you used. This documentation is crucial for transparency and reproducibility.

13. **Make Informed Decisions:**
    Finally, use your analysis to make informed decisions or take actions based on the insights gained from the central tendencies of your data.

The specific tools and software you use for data analysis may vary depending on your preferences and expertise. Common tools for data analysis include Microsoft Excel, Python with libraries like NumPy, pandas, and Matplotlib, R, and specialized statistical software packages.


3. What patterns arise from the data you are analyzing? 

dito na ata yung makukuha sa analysis 

------------------------------------------------------------------------------------------------------------------------------------------------
------------------------------------------------------------------------------------------------------------------------------------------------
------------------------------------------------------------------------------------------------------------------------------------------------

Analyzing two weeks' worth of temperature and humidity data using digital signal processing concepts, statistics, and numerical methods can provide valuable insights into the data's periodicity, central tendencies, and patterns. Here's a detailed step-by-step guide on how to approach this analysis and an outline for a paper:

**Data Preparation:**

1. **Data Collection:** Collect the temperature and humidity data over two weeks from your chosen data source. Ensure the data is in a structured format, such as a CSV file, with timestamps.

2. **Data Cleaning:** Check for missing values, outliers, and inconsistencies. Impute missing data if necessary and remove outliers that may skew the analysis.

**Data Exploration:**

3. **Data Visualization:** Create time series plots of temperature and humidity to visualize the overall trends. Plotting the data is essential to get a sense of the patterns and to identify any immediate anomalies.

4. **Periodicity Analysis:** Use digital signal processing techniques like Fourier analysis to identify periodic components in the data. Calculate the dominant frequencies and determine the primary periodicities in the dataset.

**Statistics and Numerical Methods:**

5. **Central Tendencies:** Calculate the central tendencies of the data, such as the mean, median, and standard deviation, for temperature and humidity. Break this down by time of day (morning, afternoon, evening), day of the week, and overall.

6. **Temporal Patterns:** Calculate statistical measures like autocorrelation to identify temporal patterns in the data. Determine if there are any recurring patterns during the two-week period.

**Pattern Recognition:**

7. **Clustering Analysis:** Use clustering algorithms like k-means or hierarchical clustering to group similar data points together. This can help identify clusters of temperature and humidity behavior.

8. **Time Series Decomposition:** Decompose the time series data into its components, such as trend, seasonality, and residual, using methods like the Seasonal Decomposition of Time Series (STL) or wavelet decomposition.

9. **Data Anomalies:** Identify any unusual patterns or anomalies in the data that don't conform to the expected periodic behavior. This may require statistical anomaly detection methods or machine learning algorithms.

**Paper Outline:**

1. **Introduction:**
   - Briefly introduce the data source and the motivation for the analysis.
   - State the research questions and objectives.

2. **Data Collection and Preparation:**
   - Describe the data source and collection process.
   - Explain how data cleaning and preprocessing were performed.

3. **Data Exploration:**
   - Present time series plots of temperature and humidity.
   - Discuss the identified periodic components and their significance.

4. **Statistics and Numerical Methods:**
   - Provide central tendencies for temperature and humidity.
   - Present temporal patterns, including autocorrelation and trends.

5. **Pattern Recognition:**
   - Discuss the results of clustering analysis.
   - Explain the time series decomposition and its findings.
   - Highlight any anomalies or irregular patterns.

6. **Discussion:**
   - Interpret the findings and discuss their implications.
   - Relate the periodicity to meteorological phenomena.
   - Discuss how the data can be useful for specific applications.

7. **Conclusion:**
   - Summarize the key findings.
   - Suggest possible future research directions.

8. **References:**
   - Cite relevant literature, data sources, and tools used.

9. **Appendices:**
   - Include supplementary materials like code, additional plots, or detailed statistical results.

10. **Acknowledgments:**
    - Acknowledge any data sources, funding, or individuals who contributed to the project.

Remember to use clear and concise language, present your results visually with appropriate graphs and figures, and thoroughly explain your methodology. This detailed approach will ensure a comprehensive analysis and a well-structured research paper.