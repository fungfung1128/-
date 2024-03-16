# skip-to-run
        try:
            if ticker[-2:] != "HK":
                df['SP500 RSI'] = calculate_rsi(dfsp500['Close'], period=14)
                df['NQ100 RSI'] = calculate_rsi(dfnq100['Close'], period=14)

        except Exception as e:
            print(f"Failed download: {ticker}: {e}")
            return None, None, None
