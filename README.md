# Extra
use swift soap
https://github.com/kiritmodi2702/SoapAPIDemo
souce code from this url

 NSString * customerIDFromLogin = @"12";
    
//    NSString * strURL =[NSString stringWithFormat:@"%@fun=funMethodName&customer_id=%@",WebServiceURL,customerIDFromLogin];
    NSString * strURL =[NSString stringWithFormat:@"%@fun=funTotalActiveAWR&customer_id=%@",WebServiceURL,customerIDFromLogin];
    strURL = [strURL stringByAddingPercentEscapesUsingEncoding:NSUTF8StringEncoding];
//     NSLog(@"str ==> %@",strURL);
    NSURL *url = [NSURL URLWithString:strURL];
    ASIHTTPRequest *request = [ASIHTTPRequest requestWithURL:url];
    request.tag = 1;
    [request setDelegate:self];
    [request startAsynchronous];
    [self showLoader];
