# Changelog

## v1.2.2 (2025-06-03)

### Added Exchange Passphrase Support
- Added passphrase parameter to all private API tools
- Added environment variable support for exchange passphrases
- Updated exchange manager to handle passphrases (required by some exchanges like KuCoin)
- Updated documentation with passphrase configuration examples
- Implemented passphrase as an optional parameter to maintain compatibility

## v1.2.1 (2025-04-01)

### Improved Proxy Configuration
- Updated documentation to recommend integrated proxy URL format (username:password@host)
- Enhanced proxy configuration examples in README.md and .env.example
- Maintained backward compatibility with separate username/password fields
- Improved user experience by simplifying proxy setup process

## v1.2.0 (2025-03-31)

### Added Proxy Support
- Added functions to configure and use proxies (getProxyConfig and formatProxyUrl)
- Added configuration tools to control proxy settings (set-proxy-config, test-proxy-connection)
- Added clearExchangeCache function to clear exchange cache
- Added console output redirection to stderr to avoid interfering with MCP protocol
- Created fix-mcp-errors.sh script to handle MCP communication issues

### Expanded Exchange Support
- Added more exchanges (bitget, coinex, cryptocom, etc.)
- Added derivatives market support for existing exchanges (binanceusdm, kucoinfutures, etc.)
- Added market type support (MarketType enum: spot, future, swap, option, margin)
- Added DEFAULT_MARKET_TYPE global setting
- Modified getExchange function to support different market types
- Added getExchangeWithMarketType function to get exchanges with specific market types

### Enhanced Tools
- Added leverage trading tools (set-leverage, set-margin-mode)
- Added futures market data tools (get-leverage-tiers, get-funding-rates)
- Added futures trading tools (place-futures-market-order)
- Updated existing trading tools to support market type parameters
- Added configuration tools for modifying settings at runtime (set-market-type)

### Improved Utilities
- Optimized caching system (supporting market type distinction)
- Added logging functionality with different log levels (DEBUG, INFO, WARNING, ERROR)
- Improved adaptive rate limiter to handle API rate limits
- Added dynamic request frequency adjustment based on exchange API limitations

### Other Changes
- Updated package.json version to 1.2.0
- Added rxjs dependency
- Updated related documentation and examples
