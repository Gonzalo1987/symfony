CHANGELOG
=========

5.4
---

 * Deprecate `AnonymousToken`, as the related authenticator was deprecated in 5.3
 * Deprecate `Token::getCredentials()`, tokens should no longer contain credentials (as they represent authenticated sessions)
 * Deprecate returning `string|\Stringable` from `Token::getUser()` (it must return a `UserInterface`)
 * Deprecate `AuthenticatedVoter::IS_AUTHENTICATED_ANONYMOUSLY` and `AuthenticatedVoter::IS_ANONYMOUS`,
   use `AuthenticatedVoter::IS_AUTHENTICATED_FULLY` or `AuthenticatedVoter::IS_AUTHENTICATED` instead.
 * Deprecate `AuthenticationTrustResolverInterface::isAnonymous()` and the `is_anonymous()` expression
   function as anonymous no longer exists in version 6, use the `isFullFledged()` or the new
   `isAuthenticated()` instead if you want to check if the request is (fully) authenticated.
 * Deprecate the `$authenticationManager` argument of the `AuthorizationChecker` constructor
 * Deprecate setting the `$alwaysAuthenticate` argument to `true` and not setting the
   `$exceptionOnNoToken` argument to `false` of `AuthorizationChecker`
 * Deprecate methods `TokenInterface::isAuthenticated()` and `setAuthenticated`,
   tokens will always be considered authenticated in 6.0

5.3
---

The CHANGELOG for version 5.3 and earlier can be found at https://github.com/symfony/symfony/blob/5.3/src/Symfony/Component/Security/CHANGELOG.md