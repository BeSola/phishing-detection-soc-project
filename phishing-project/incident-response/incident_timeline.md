| Time   |   Event Description                                              | Log Source      |

|--------|------------------------------------------------------------    |----------------|

| 09:12  |   Phishing emails delivered to mjackson, whouston, bmarley       | email\_logs     |

| 09:15  |   User mjackson clicked phishing URL                             | proxy\_logs     |

| 09:16  |   User jdoe clicked phishing URL                                 | proxy\_logs     |

| 09:18  |   Failed login attempts detected for mjackson from IP 185.220.101.5   | auth\_logs      |

| 09:19  |   mjackson successful login (possible credential compromise)      | auth\_logs      |

| 09:21  |   Failed login attempts detected for jdoe from IP 185.220.101.5   | auth\_logs      |

| 09:25  |   SOC detection logic flagged abnormal login patterns               | detections     |

| 09:30  |   SOC analyst initiates response: password resets, block malicious domain | incident\_response |


