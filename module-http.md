# Mammoth HTTP

## Request

    $request->getUserAgent();
    $request->getURL();
    $request->getProtocol();
    $request->getProtocol(); [http, https]
    $request->getHost();
    $request->getURI();
    $request->getReferer();
    $request->getIP();
    $request->getRequestedWith(); [ajax etc...
    $request->getDoNotTrack(); DNT etc
    $request->getAccepts(); return array of acceptable types
    $request->getLanguage(); the user language
    $request->getEncoding(); the user encoding
    $request->getContentType(); the user accepted content type




    $request->post([$key]);
    $request->get([$key]);
    $request->request([$key]);
    $request->cookie([$key]);;
    $request->file([$key]);?????????????