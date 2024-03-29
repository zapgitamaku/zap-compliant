# Table of contents

* [Welcome to ZapAPI!](README.md)
* [Quick Start](quick-start/README.md)
  * [Authentication](quick-start/authentication/README.md)
    * [API Keys](quick-start/authentication/api-keys.md)
  * [Error](quick-start/error.md)
* [USER Service](user-service/README.md)
  * [Create User](user-service/create-user.md)
  * [Log In User](user-service/log-in-user.md)
  * [Google Log In](user-service/google-log-in.md)
  * [Google Log In- App](user-service/google-log-in-app.md)
  * [Apple Log In- App](user-service/apple-log-in-app.md)
  * [Refresh User Token](user-service/refresh-user-token.md)
  * [Log In User with 2FA Token](user-service/log-in-user-with-2fa-token.md)
  * [Enable 2 Factor Authentication](user-service/enable-2-factor-authentication.md)
  * [Verify 2 Factor Authentication](user-service/verify-2-factor-authentication.md)
  * [Disable 2 Factor Authentication](user-service/disable-2-factor-authentication.md)
  * [Fetch Users](user-service/fetch-users.md)
  * [Fetch Users By Id](user-service/fetch-users-by-id.md)
  * [WebApp Logout User By Id](user-service/webapp-logout-user-by-id.md)
  * [Fetch Referred Users Count](user-service/fetch-referred-users-count.md)
  * [Fetch Successful Referred Users](user-service/fetch-successful-referred-users.md)
  * [Fetch Referral Amount Earned](user-service/fetch-referral-amount-earned.md)
  * [Fetch Users Details from Jwt](user-service/fetch-users-details-from-jwt.md)
  * [Edit User By Id](user-service/edit-user-by-id.md)
  * [Edit User Phone Number By Id](user-service/edit-user-phone-number-by-id.md)
  * [LogOut User By Id](user-service/logout-user-by-id.md)
  * [User Adds NPS](user-service/user-adds-nps.md)
  * [Edit UserBVNBy Id](user-service/edit-userbvnby-id.md)
  * [Edit Guest By Id](user-service/edit-guest-by-id.md)
  * [Delete User By Id](user-service/delete-user-by-id.md)
  * [Change User Password](user-service/change-user-password.md)
  * [Reset User Password](user-service/reset-user-password.md)
  * [View Tooltip Update](user-service/view-tooltip-update.md)
  * [View Username Update](user-service/view-username-update.md)
* [Affiliate Service](affiliate-service/README.md)
  * [Create Affiliate](affiliate-service/create-affiliate.md)
  * [Fetch Affiliate Amount Earned](affiliate-service/fetch-affiliate-amount-earned.md)
  * [Fetch Affiliate By Id](affiliate-service/fetch-affiliate-by-id.md)
* [OTP Service](otp-service/README.md)
  * [Generate OTP](otp-service/generate-otp.md)
  * [Resend OTP](otp-service/resend-otp.md)
  * [Forgot Password](otp-service/forgot-password.md)
  * [Verify OTP](otp-service/verify-otp.md)
* [App Version](app-version/README.md)
  * [Fetch Latest App Version](app-version/fetch-latest-app-version.md)
* [BANK Service](bank-service/README.md)
  * [Add Bank](bank-service/add-bank.md)
  * [Fetch Banks](bank-service/fetch-banks.md)
  * [Fetch Bank by Id](bank-service/fetch-bank-by-id.md)
  * [Edit Bank by Id](bank-service/edit-bank-by-id.md)
  * [Delete Bank by Id](bank-service/delete-bank-by-id.md)
* [BANK Detail Service](bank-detail-service/README.md)
  * [Add Bank Details](bank-detail-service/add-bank-details.md)
  * [Fetch Bank Details](bank-detail-service/fetch-bank-details.md)
  * [Fetch Bank Details by Id\*](bank-detail-service/fetch-bank-details-by-id.md)
  * [Fetch Bank Details by UserId\*](bank-detail-service/fetch-bank-details-by-userid.md)
  * [Edit Bank Details By Id](bank-detail-service/edit-bank-details-by-id.md)
  * [Resolve Bank Details](bank-detail-service/resolve-bank-details.md)
  * [Delete Bank Details By Id](bank-detail-service/delete-bank-details-by-id.md)
* [CURRENCY Service](currency-service/README.md)
  * [Add Currency](currency-service/add-currency.md)
  * [Fetch Currencies](currency-service/fetch-currencies.md)
  * [Fetch LandingPage Currencies](currency-service/fetch-landingpage-currencies.md)
  * [Fetch Currency by Id](currency-service/fetch-currency-by-id.md)
  * [Fetch Currency by Ticker](currency-service/fetch-currency-by-ticker.md)
  * [Edit Currency by Id](currency-service/edit-currency-by-id.md)
  * [Delete Currency by Id](currency-service/delete-currency-by-id.md)
* [FAQ Article Service](faq-article-service/README.md)
  * [Add FAQ Article](faq-article-service/add-faq-article.md)
  * [Fetch FAQ Articles](faq-article-service/fetch-faq-articles.md)
  * [Fetch FAQ Article by Id](faq-article-service/fetch-faq-article-by-id.md)
  * [Fetch FAQ Articles by category](faq-article-service/fetch-faq-articles-by-category.md)
  * [Fetch FAQ Articles by search query](faq-article-service/fetch-faq-articles-by-search-query.md)
  * [Edit FAQ Article by id](faq-article-service/edit-faq-article-by-id.md)
  * [Delete FAQ Article by Id](faq-article-service/delete-faq-article-by-id.md)
* [TRADE Service](trade-service/README.md)
  * [Add Trade](trade-service/add-trade.md)
  * [Fetch Trades](trade-service/fetch-trades.md)
  * [Fetch Trades by Id](trade-service/fetch-trades-by-id.md)
  * [Fetch Trades by Order Id](trade-service/fetch-trades-by-order-id.md)
  * [Update Trade](trade-service/update-trade.md)
  * [Delete Trade](trade-service/delete-trade.md)
* [MARKET Service](market-service/README.md)
  * [Add Market](market-service/add-market.md)
  * [Fetch Market\*](market-service/fetch-market.md)
  * [Fetch Market by Id](market-service/fetch-market-by-id.md)
  * [Update Market by Id](market-service/update-market-by-id.md)
  * [Delete Market by Id](market-service/delete-market-by-id.md)
* [ORDER Service](order-service/README.md)
  * [Create Order](order-service/create-order.md)
  * [Fetch Orders](order-service/fetch-orders.md)
  * [Fetch Orders By Id](order-service/fetch-orders-by-id.md)
  * [Fetch Orders By User Id](order-service/fetch-orders-by-user-id.md)
  * [Fetch Orders By User Id with filter](order-service/fetch-orders-by-user-id-with-filter.md)
  * [Update Order by Id](order-service/update-order-by-id.md)
  * [Add Order Rating](order-service/add-order-rating.md)
  * [Refund Order by Id](order-service/refund-order-by-id.md)
  * [Process Order by Id](order-service/process-order-by-id.md)
  * [Delete Order by Id](order-service/delete-order-by-id.md)
* [VERIFICATION Service](verification-service/README.md)
  * [Create ID Verification](verification-service/create-id-verification.md)
  * [Create Residence Verification](verification-service/create-residence-verification.md)
  * [Upload Verification](verification-service/upload-verification.md)
  * [Fetch Verifications](verification-service/fetch-verifications.md)
  * [Fetch Verifications Provider status](verification-service/fetch-verifications-provider-status.md)
  * [Update Verifications Provider status](verification-service/update-verifications-provider-status.md)
  * [Fetch Verification by Id](verification-service/fetch-verification-by-id.md)
  * [Fetch Verification by user Id](verification-service/fetch-verification-by-user-id.md)
  * [Update Verification by Id](verification-service/update-verification-by-id.md)
  * [Delete Verification by Id](verification-service/delete-verification-by-id.md)
* [PAYOUT Service](payout-service/README.md)
  * [Create Referral Payout](payout-service/create-referral-payout.md)
  * [Create Affiliate Payout](payout-service/create-affiliate-payout.md)
* [RATE Engine](rate-engine/README.md)
  * [Get Rate](rate-engine/get-rate.md)
  * [Get Rate With Currencies](rate-engine/get-rate-with-currencies.md)
  * [Get Rate With Currencies(USD amount)](rate-engine/get-rate-with-currencies-usd-amount.md)
  * [Get Rate With Currencies Reversed](rate-engine/get-rate-with-currencies-reversed.md)
  * [Price Feed](rate-engine/price-feed.md)
* [Support Conversation Service](support-conversation-service/README.md)
  * [Create New Support Conversation](support-conversation-service/create-new-support-conversation.md)
  * [Fetch Support Conversations by userId](support-conversation-service/fetch-support-conversations-by-userid.md)
  * [Fetch Support Conversations by supportId](support-conversation-service/fetch-support-conversations-by-supportid.md)
  * [Fetch All Support Conversations](support-conversation-service/fetch-all-support-conversations.md)
  * [Fetch Support Conversation by id](support-conversation-service/fetch-support-conversation-by-id.md)
  * [Close Support Conversations by id](support-conversation-service/close-support-conversations-by-id.md)
  * [ReOpenSupport Conversations by id](support-conversation-service/reopensupport-conversations-by-id.md)
  * [Edit Support Conversation by id](support-conversation-service/edit-support-conversation-by-id.md)
  * [Delete Support Conversation by id](support-conversation-service/delete-support-conversation-by-id.md)
  * [Add Conversation Rating](support-conversation-service/add-conversation-rating.md)
* [Support Message Service](support-message-service/README.md)
  * [Create New Support Message](support-message-service/create-new-support-message.md)
  * [Create Support User New Response Message](support-message-service/create-support-user-new-response-message.md)
  * [Fetch Support Messages by conversationId](support-message-service/fetch-support-messages-by-conversationid.md)
  * [Fetch Support Message by id](support-message-service/fetch-support-message-by-id.md)
  * [Edit Support Message by id](support-message-service/edit-support-message-by-id.md)
  * [Delete Support Message by id (soft)](support-message-service/delete-support-message-by-id-soft.md)
* [ZAP Socket Service](zap-socket-service/README.md)
  * [WebSockets](zap-socket-service/websockets.md)
* [Zap List Service](zap-waitlist-service/README.md)
  * [Create New Waiting User](zap-waitlist-service/create-new-waiting-user.md)
  * [Add New User to Newsletter List](zap-waitlist-service/create-new-waiting-user-1.md)
  * [Fetch All Waiting Users](zap-waitlist-service/fetch-all-waiting-users.md)
* [NOTIFICATION SERVICE](notification-service/README.md)
  * [Fetch System Notifications](notification-service/fetch-system-notifications.md)
  * [Fetch Security Notifications](notification-service/fetch-security-notifications.md)

## Reference

* [API Reference](reference/api-reference.md)
