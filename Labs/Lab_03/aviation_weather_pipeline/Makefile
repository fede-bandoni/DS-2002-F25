.PHONY: all fetch analyze clean

# Default target
all: analyze

fetch:
	@echo "-- Fetching METAR data. --"
	./fetch_metars.sh
	@echo "-- Fetch complete, raw data saved in 'raw_metars/' --"

analyze: fetch
	@echo "-- Analyzing METAR data. --"
	./analyze_data.sh
	@echo "-- Analysis complete. Results saved in 'weather_report.csv' --"
	@echo "-- Pipeline finished successfully! --"

clean:
	@echo "-- Cleaning up generated files. --"
	rm -rf raw_metars weather_report.csv
	@echo "-- Clean complete. Workspace reset. --"

