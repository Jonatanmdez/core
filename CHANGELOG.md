# CHANGELOG

## 0.2.0 

> Date: *20xx-xx-xx* (unreleased)
    
* New dependency: ``"symfony/css-selector": "^2|^3"``
    
* breaking changes
  * url interface was refactored [#22](https://github.com/serp-spider/core/pull/22)
    * Internal structure is better (no construct in the interface)
    * now ``port`` and ``user:pass auth``  are supported [#18](https://github.com/serp-spider/core/issues/18) 
    * resolve and resolveAsString are now 2 distinct methods. [#19](https://github.com/serp-spider/core/issues/19)
    * resolve does not support string anymore [d56cbc39e710735296bbdd675431f7b3e87f534c](https://github.com/serp-spider/core/commit/d56cbc39e710735296bbdd675431f7b3e87f534c#diff-2bb04ebe8ec8dc8575afdd6a7a0bc0f6L325)
    * new method ``UrlArchiveInterface::getAuthority``
    * url resolution is now compatible with rfc3986
    * query params now accept empty value [7233b7d1b67ed2a061746c210171b121ac931bb9](https://github.com/serp-spider/core/commit/7233b7d1b67ed2a061746c210171b121ac931bb9#diff-ea6d1c5de04976abd5f773367a57da23R79)
    * fix a bug with query params that are number only [#25](https://github.com/serp-spider/core/pull/25) 
  * cookie expiration time was not on the same standard everywhere [#13](https://github.com/serp-spider/core/pull/13)
  
* Additions
  * Css parser was moved from google package to core [2f7d022d6da4905519a02d65c2f262aefc8b6bbf](https://github.com/serp-spider/core/commit/2f7d022d6da4905519a02d65c2f262aefc8b6bbf)
  * ``Dom`` component that offers better parsing of the dom (replacement for the ``googleDom`` class from google package) [view  commits](https://github.com/serp-spider/core/compare/2f7d022d6da4905519a02d65c2f262aefc8b6bbf...22749d020c953e987dedc452566b4973923bf439)
  * ``RequestBuilder`` class that allows to construct PSR7 request from installed packages (``zendframework/zend-diactoros`` or ``guzzlehttp/psr7``) 
  [98ab9f56bcef0ac36bae2b43cd965d14522a3294](https://github.com/serp-spider/core/commit/98ab9f56bcef0ac36bae2b43cd965d14522a3294)


------------------
