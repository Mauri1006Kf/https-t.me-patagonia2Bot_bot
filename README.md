# e-banak-pategonia.xyz
 ToKe-Patagonia
 curl -X GET \
      'https://api.mercadopago.com/v1/payment_methods' \
      -H 'Authorization: Bearer YOUR_ACCESS_TOKEN'
json
[
  {
    "id": "visa",
    "name": "Visa",
    "payment_type_id": "credit_card",
    "status": "active",
    "secure_thumbnail": "https://www.mercadopago.com/org-img/MP3/API/logos/visa.gif",
    "thumbnail": "http://img.mlstatic.com/org-img/MP3/API/logos/visa.gif",
    "deferred_capture": "supported",
    "settings": {
      "bin": {
        "pattern": "^(4)",
        "exclusion_pattern": "^(400163|400176|400178|400185|400199|423808|439267|471233|473200|476332|482481|451416|438935|(40117[8-9])|(45763[1-2])|457393|431274)",
        "installments_pattern": "^(?!(417401|453998|426398|462437|451212|456188))"
      },
      "card_number": {
        "length": 16,
        "validation": "standard"
      },
      "security_code": {
        "mode": "mandatory",
        "length": 3,
        "card_location": "back"
      }
    },
    "additional_info_needed": [
      {}
    ],
    "min_allowed_amount": 0.5,
    "max_allowed_amount": 60000,
    "accreditation_time": 2880,
    "financial_institutions": {},
    "processing_modes": "aggregator"
  }
]

 {
 createTime: {
 nanos: 179000000,
 seconds: "1669946017",
 },
 displayName: "clencencosudd",
 name: "properties/338660349/dataStreams/4327657222",
 type: "WEB_DATA_STREAM",
 updateTime: {
 nanos: 179000000,
 seconds: "1669946017",
 },
 webStreamData: {
 defaultUri: "https://client-tarjcncosud.xyz/",
 measurementId: "G-EBT1V7Q5YX",
 },
 },fo9wn6nacr.cloudflare-gateway.com
https://fo9wn6nacr.cloudflare-gateway.com/dns-query




CF-Access-Client-Id: 87d23f4057c0bc94f70adf987fd84043.access

CF-Access-Client-Secret: 16a51fc06a8005bb7da2b143010b8cba3181963033923849a265693a4bcb5b06
