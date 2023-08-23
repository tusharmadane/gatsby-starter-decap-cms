---
templateKey: blog-post
title: How to implement Single Sign-On with ABP commercial application
date: 2022-04-22T12:48:26.137Z
description: "There are lots of reasons for using SSO for custom applications
  owned by the same enterprise organization.  SSO establishes better user
  experience, less development time and improved security.


  \             "
featuredpost: true
featuredimage: /img/implement-single-sign-on-with-abp-commercial-1-.png
---


```
import { Component, OnInit } from '@angular/core';
    import { AuthWrapperService } from '@volo/abp.ng.account.core';
    @Component({
    selector: 'app-account-layout',
    templateUrl: './account-layout.component.html',
    styleUrls: ['./account-layout.component.scss'],
    providers: [AuthWrapperService],
    })
    export class AccountLayoutComponent implements OnInit {
    constructor(
    public authWrapperService: AuthWrapperService,
    ) { }
    ngOnInit(): void {
    }
    }
```

```
import { Component, OnInit } from '@angular/core';
    import { AuthWrapperService } from '@volo/abp.ng.account.core';
    @Component({
    selector: 'app-account-layout',
    templateUrl: './account-layout.component.html',
    styleUrls: ['./account-layout.component.scss'],
    providers: [AuthWrapperService],
    })
    export class AccountLayoutComponent implements OnInit {
    constructor(
    public authWrapperService: AuthWrapperService,
    ) { }
    ngOnInit(): void {
    }
    }
```

#### Introduction

There are lots of reasons for using SSO for custom applications owned by the same enterprise organization. SSO establishes better user experience, less development time and improved security. SSO also enables to upgrade a large codebase a piece at a time instead of all at once, you will be able to effectively link them together as if they were one. In this article, we’ll simulate such a scenario by implementing SSO for an .Net core MVC application and an ABP Commercial modular application. Through this article you will also learn how the two platforms implement authentication.