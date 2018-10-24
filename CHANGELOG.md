## Version 1.1.2 (2018-10-12)

Eko Messaging SDK `1.1.2` is released.

#### Bug Fixes

* Fixed `EkoChannel` collection with the filter `EkoChannelFilter.NOT_MEMBER` contains channel you joined.
* Fixed `EkoChannel` data not update in real-time.


## Version 1.1.0 (2018-10-05)

Eko Messaging SDK `1.1.0` is released.

#### Breaking Changes

* The parameterless `EkoChannelRepository.getChannelCollection()` method now required a single parameter of `EkoChannelFilter`.

#### API / Behavior Changes

* Delete message
* Unread message count
* You can create a `EkoChannel` collection that contains
  * `EkoChannelFilter.MEMBER`: channels that you have joined.
  * `EkoChannelFilter.NOT_MEMBER`: channels in the system which you haven't joined.
  * `EkoChannelFilter.ALL`: all channels.
* Live Reading: Eko Messaging SDK now supports live reading mode. When you are in live reading mode, all new message are marked as read automatically.
  * `EkoChannel.membership().startReading()`: enables live reading mode. Should be called in `onResume()` method.
  * `EkoChannel.membership().stopReading()`: disables live reading mode. Should be called in `onPause()` method.

#### Deprecations

* `EkoMessageRepository.getCount()` is deprecated.
* `EkoMessageRepository.getCount(String channel)` is deprecated.


## Version 1.0.2 (2018-08-28)

Eko Messaging SDK `1.0.2` is released with improved network bandwidth efficiency.

#### Bug Fixes

* Fixed `EkoMessage.getUser()` returns `null` instead of `EkoUser` the sender of the message.


## Version 1.0.1 (2018-07-11)

Eko Messaging SDK `1.0.1` is released with internal changes.


## Version 1.0.0 (2018-07-10)

Eko Messaging SDK `1.0.0` is released.
