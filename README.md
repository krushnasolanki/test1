{
  "annotations": {
    "list": [
      {
        "builtIn": 1,
        "datasource": {
          "type": "datasource",
          "uid": "grafana"
        },
        "enable": true,
        "hide": true,
        "iconColor": "rgba(0, 211, 255, 1)",
        "name": "Annotations & Alerts",
        "target": {
          "limit": 100,
          "matchAny": false,
          "tags": [],
          "type": "dashboard"
        },
        "type": "dashboard"
      }
    ]
  },
  "editable": true,
  "fiscalYearStartMonth": 0,
  "graphTooltip": 0,
  "id": 30,
  "links": [],
  "liveNow": false,
  "panels": [
    {
      "datasource": {
        "type": "prometheus",
        "uid": "000000003"
      },
      "fieldConfig": {
        "defaults": {
          "color": {
            "mode": "thresholds"
          },
          "mappings": [],
          "thresholds": {
            "mode": "absolute",
            "steps": [
              {
                "color": "green",
                "value": null
              },
              {
                "color": "red",
                "value": 80
              }
            ]
          }
        },
        "overrides": []
      },
      "gridPos": {
        "h": 4,
        "w": 3,
        "x": 0,
        "y": 0
      },
      "id": 534,
      "options": {
        "colorMode": "none",
        "graphMode": "none",
        "justifyMode": "center",
        "orientation": "auto",
        "reduceOptions": {
          "calcs": [
            "lastNotNull"
          ],
          "fields": "",
          "values": false
        },
        "textMode": "auto"
      },
      "pluginVersion": "9.0.4",
      "targets": [
        {
          "datasource": {
            "type": "prometheus",
            "uid": "000000003"
          },
          "exemplar": true,
          "expr": "sum(kube_pod_status_phase{namespace=~\"$namespace\",cluster=~\"$cluster\",job=~\"kube-state-metrics\",phase=\"Running\"})",
          "interval": "",
          "legendFormat": "",
          "refId": "A"
        }
      ],
      "title": "Pods Running",
      "type": "stat"
    },
    {
      "datasource": {
        "type": "prometheus",
        "uid": "000000003"
      },
      "fieldConfig": {
        "defaults": {
          "color": {
            "mode": "thresholds"
          },
          "mappings": [],
          "thresholds": {
            "mode": "absolute",
            "steps": [
              {
                "color": "green",
                "value": null
              },
              {
                "color": "red",
                "value": 80
              }
            ]
          }
        },
        "overrides": []
      },
      "gridPos": {
        "h": 4,
        "w": 3,
        "x": 3,
        "y": 0
      },
      "id": 533,
      "options": {
        "colorMode": "none",
        "graphMode": "none",
        "justifyMode": "center",
        "orientation": "auto",
        "reduceOptions": {
          "calcs": [
            "lastNotNull"
          ],
          "fields": "",
          "values": false
        },
        "textMode": "auto"
      },
      "pluginVersion": "9.0.4",
      "targets": [
        {
          "datasource": {
            "type": "prometheus",
            "uid": "000000003"
          },
          "exemplar": true,
          "expr": " sum(kube_pod_status_phase{namespace=~\"$namespace\", cluster=~\"$cluster\", job=~\"kube-state-metrics\",phase=\"Failed\"})",
          "interval": "",
          "legendFormat": "",
          "refId": "A"
        }
      ],
      "title": "Pods Failed",
      "type": "stat"
    },
    {
      "datasource": {
        "type": "prometheus",
        "uid": "000000003"
      },
      "fieldConfig": {
        "defaults": {
          "color": {
            "mode": "thresholds"
          },
          "mappings": [],
          "thresholds": {
            "mode": "absolute",
            "steps": [
              {
                "color": "green",
                "value": null
              },
              {
                "color": "red",
                "value": 80
              }
            ]
          }
        },
        "overrides": []
      },
      "gridPos": {
        "h": 4,
        "w": 3,
        "x": 6,
        "y": 0
      },
      "id": 535,
      "options": {
        "colorMode": "none",
        "graphMode": "none",
        "justifyMode": "center",
        "orientation": "auto",
        "reduceOptions": {
          "calcs": [
            "lastNotNull"
          ],
          "fields": "",
          "values": false
        },
        "textMode": "auto"
      },
      "pluginVersion": "9.0.4",
      "targets": [
        {
          "datasource": {
            "type": "prometheus",
            "uid": "000000003"
          },
          "exemplar": true,
          "expr": " sum(kube_pod_status_phase{namespace=~\"$namespace\", cluster=~\"$cluster\",job=~\"kube-state-metrics\",phase=\"Pending\"})",
          "interval": "",
          "legendFormat": "",
          "refId": "A"
        }
      ],
      "title": "Pods Pending",
      "type": "stat"
    },
    {
      "datasource": {
        "type": "prometheus",
        "uid": "000000003"
      },
      "fieldConfig": {
        "defaults": {
          "color": {
            "mode": "thresholds"
          },
          "mappings": [],
          "thresholds": {
            "mode": "absolute",
            "steps": [
              {
                "color": "green",
                "value": null
              },
              {
                "color": "red",
                "value": 80
              }
            ]
          }
        },
        "overrides": []
      },
      "gridPos": {
        "h": 4,
        "w": 3,
        "x": 9,
        "y": 0
      },
      "id": 536,
      "options": {
        "colorMode": "none",
        "graphMode": "none",
        "justifyMode": "auto",
        "orientation": "horizontal",
        "reduceOptions": {
          "calcs": [
            "lastNotNull"
          ],
          "fields": "",
          "values": false
        },
        "textMode": "auto"
      },
      "pluginVersion": "9.0.4",
      "targets": [
        {
          "datasource": {
            "type": "prometheus",
            "uid": "000000003"
          },
          "exemplar": true,
          "expr": "sum(kube_pod_container_status_running{namespace=~\"$namespace\",cluster=~\"$cluster\",job=~\"kube-state-metrics\",container!=\"POD\"})",
          "interval": "",
          "legendFormat": "",
          "refId": "A"
        }
      ],
      "title": "Containers Running",
      "type": "stat"
    },
    {
      "datasource": {
        "type": "prometheus",
        "uid": "000000003"
      },
      "fieldConfig": {
        "defaults": {
          "color": {
            "mode": "thresholds"
          },
          "mappings": [],
          "thresholds": {
            "mode": "absolute",
            "steps": [
              {
                "color": "green",
                "value": null
              },
              {
                "color": "red",
                "value": 80
              }
            ]
          }
        },
        "overrides": []
      },
      "gridPos": {
        "h": 4,
        "w": 3,
        "x": 12,
        "y": 0
      },
      "id": 537,
      "options": {
        "colorMode": "none",
        "graphMode": "none",
        "justifyMode": "auto",
        "orientation": "horizontal",
        "reduceOptions": {
          "calcs": [
            "lastNotNull"
          ],
          "fields": "",
          "values": false
        },
        "textMode": "auto"
      },
      "pluginVersion": "9.0.4",
      "targets": [
        {
          "datasource": {
            "type": "prometheus",
            "uid": "000000003"
          },
          "exemplar": true,
          "expr": "sum(kube_pod_container_status_terminated{namespace=~\"$namespace\",cluster=~\"$cluster\",job=~\"kube-state-metrics\",container!=\"POD\"})",
          "interval": "",
          "legendFormat": "",
          "refId": "A"
        }
      ],
      "title": "Containers Terminated",
      "type": "stat"
    },
    {
      "datasource": {
        "type": "prometheus",
        "uid": "000000003"
      },
      "fieldConfig": {
        "defaults": {
          "color": {
            "mode": "thresholds"
          },
          "mappings": [],
          "thresholds": {
            "mode": "absolute",
            "steps": [
              {
                "color": "green",
                "value": null
              },
              {
                "color": "red",
                "value": 80
              }
            ]
          }
        },
        "overrides": []
      },
      "gridPos": {
        "h": 4,
        "w": 3,
        "x": 15,
        "y": 0
      },
      "id": 538,
      "options": {
        "colorMode": "none",
        "graphMode": "none",
        "justifyMode": "auto",
        "orientation": "horizontal",
        "reduceOptions": {
          "calcs": [
            "lastNotNull"
          ],
          "fields": "",
          "values": false
        },
        "textMode": "auto"
      },
      "pluginVersion": "9.0.4",
      "targets": [
        {
          "datasource": {
            "type": "prometheus",
            "uid": "000000003"
          },
          "exemplar": true,
          "expr": "sum(kube_pod_container_status_waiting{namespace=~\"$namespace\",cluster=~\"$cluster\",job=~\"kube-state-metrics\",container!=\"POD\"})",
          "interval": "",
          "legendFormat": "",
          "refId": "A"
        }
      ],
      "title": "Containers waiting",
      "type": "stat"
    },
    {
      "collapsed": true,
      "datasource": {
        "type": "prometheus",
        "uid": "000000003"
      },
      "gridPos": {
        "h": 1,
        "w": 24,
        "x": 0,
        "y": 4
      },
      "id": 192,
      "panels": [
        {
          "datasource": {
            "type": "prometheus",
            "uid": "000000003"
          },
          "fieldConfig": {
            "defaults": {
              "color": {
                "mode": "thresholds"
              },
              "mappings": [],
              "thresholds": {
                "mode": "absolute",
                "steps": [
                  {
                    "color": "green"
                  },
                  {
                    "color": "red",
                    "value": 80
                  }
                ]
              }
            },
            "overrides": []
          },
          "gridPos": {
            "h": 4,
            "w": 2,
            "x": 0,
            "y": 5
          },
          "id": 198,
          "options": {
            "colorMode": "none",
            "graphMode": "none",
            "justifyMode": "center",
            "orientation": "auto",
            "reduceOptions": {
              "calcs": [
                "lastNotNull"
              ],
              "fields": "",
              "values": false
            },
            "textMode": "value"
          },
          "pluginVersion": "9.0.4",
          "targets": [
            {
              "datasource": {
                "type": "prometheus",
                "uid": "000000003"
              },
              "editorMode": "code",
              "exemplar": true,
              "expr": "count(node_uname_info{cluster=~\"$cluster\"})",
              "hide": true,
              "interval": "",
              "legendFormat": "",
              "range": true,
              "refId": "A"
            },
            {
              "datasource": {
                "type": "prometheus",
                "uid": "000000003"
              },
              "editorMode": "code",
              "exemplar": true,
              "expr": "count(node_uname_info{cluster=~\"$cluster\",component=\"node-exporter\"})",
              "hide": false,
              "interval": "",
              "legendFormat": "",
              "range": true,
              "refId": "B"
            }
          ],
          "title": "#Nodes",
          "type": "stat"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "000000003"
          },
          "fieldConfig": {
            "defaults": {
              "color": {
                "mode": "thresholds"
              },
              "mappings": [],
              "thresholds": {
                "mode": "absolute",
                "steps": [
                  {
                    "color": "green"
                  },
                  {
                    "color": "red",
                    "value": 80
                  }
                ]
              }
            },
            "overrides": []
          },
          "gridPos": {
            "h": 4,
            "w": 2,
            "x": 2,
            "y": 5
          },
          "id": 206,
          "options": {
            "colorMode": "none",
            "graphMode": "none",
            "justifyMode": "center",
            "orientation": "auto",
            "reduceOptions": {
              "calcs": [
                "lastNotNull"
              ],
              "fields": "",
              "values": false
            },
            "textMode": "value"
          },
          "pluginVersion": "9.0.4",
          "targets": [
            {
              "datasource": {
                "type": "prometheus",
                "uid": "000000003"
              },
              "exemplar": true,
              "expr": "count(kube_namespace_labels{cluster=~\"$cluster\",job=~\"kube-state-metrics\"})",
              "interval": "",
              "legendFormat": "",
              "refId": "A"
            }
          ],
          "title": "#Namespaces",
          "type": "stat"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "000000003"
          },
          "fieldConfig": {
            "defaults": {
              "color": {
                "mode": "thresholds"
              },
              "mappings": [],
              "thresholds": {
                "mode": "absolute",
                "steps": [
                  {
                    "color": "green"
                  },
                  {
                    "color": "red",
                    "value": 80
                  }
                ]
              }
            },
            "overrides": []
          },
          "gridPos": {
            "h": 4,
            "w": 2,
            "x": 4,
            "y": 5
          },
          "id": 369,
          "options": {
            "colorMode": "none",
            "graphMode": "none",
            "justifyMode": "center",
            "orientation": "auto",
            "reduceOptions": {
              "calcs": [
                "lastNotNull"
              ],
              "fields": "",
              "values": false
            },
            "textMode": "value"
          },
          "pluginVersion": "9.0.4",
          "targets": [
            {
              "datasource": {
                "type": "prometheus",
                "uid": "000000003"
              },
              "exemplar": true,
              "expr": "count(namespace_workload_pod:kube_pod_owner:relabel{cluster=~\"$cluster\"})",
              "interval": "",
              "legendFormat": "",
              "refId": "A"
            }
          ],
          "title": "#Workloads",
          "type": "stat"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "000000003"
          },
          "fieldConfig": {
            "defaults": {
              "color": {
                "mode": "thresholds"
              },
              "mappings": [],
              "thresholds": {
                "mode": "absolute",
                "steps": [
                  {
                    "color": "green"
                  },
                  {
                    "color": "red",
                    "value": 80
                  }
                ]
              }
            },
            "overrides": []
          },
          "gridPos": {
            "h": 4,
            "w": 2,
            "x": 6,
            "y": 5
          },
          "id": 199,
          "options": {
            "colorMode": "none",
            "graphMode": "none",
            "justifyMode": "center",
            "orientation": "auto",
            "reduceOptions": {
              "calcs": [
                "lastNotNull"
              ],
              "fields": "",
              "values": false
            },
            "textMode": "value"
          },
          "pluginVersion": "9.0.4",
          "targets": [
            {
              "datasource": {
                "type": "prometheus",
                "uid": "000000003"
              },
              "exemplar": true,
              "expr": "count(kube_pod_info{cluster=~\"$cluster\",job=~\"kube-state-metrics\",})",
              "interval": "",
              "legendFormat": "",
              "refId": "A"
            }
          ],
          "title": "#Pods",
          "type": "stat"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "000000003"
          },
          "fieldConfig": {
            "defaults": {
              "color": {
                "mode": "thresholds"
              },
              "mappings": [],
              "thresholds": {
                "mode": "absolute",
                "steps": [
                  {
                    "color": "green"
                  },
                  {
                    "color": "red",
                    "value": 80
                  }
                ]
              }
            },
            "overrides": []
          },
          "gridPos": {
            "h": 4,
            "w": 2,
            "x": 8,
            "y": 5
          },
          "id": 203,
          "options": {
            "colorMode": "none",
            "graphMode": "none",
            "justifyMode": "center",
            "orientation": "auto",
            "reduceOptions": {
              "calcs": [
                "lastNotNull"
              ],
              "fields": "",
              "values": false
            },
            "textMode": "value"
          },
          "pluginVersion": "9.0.4",
          "targets": [
            {
              "datasource": {
                "type": "prometheus",
                "uid": "000000003"
              },
              "exemplar": true,
              "expr": "count(kube_pod_container_info{cluster=~\"$cluster\",job=~\"kube-state-metrics\"})",
              "interval": "",
              "legendFormat": "",
              "refId": "A"
            }
          ],
          "title": "#Containers",
          "type": "stat"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "000000003"
          },
          "fieldConfig": {
            "defaults": {
              "color": {
                "mode": "thresholds"
              },
              "decimals": 0,
              "mappings": [],
              "thresholds": {
                "mode": "absolute",
                "steps": [
                  {
                    "color": "green"
                  },
                  {
                    "color": "red",
                    "value": 80
                  }
                ]
              },
              "unit": "percentunit"
            },
            "overrides": []
          },
          "gridPos": {
            "h": 4,
            "w": 3,
            "x": 10,
            "y": 5
          },
          "id": 412,
          "interval": "1m",
          "links": [],
          "options": {
            "colorMode": "value",
            "graphMode": "area",
            "justifyMode": "auto",
            "orientation": "auto",
            "reduceOptions": {
              "calcs": [
                "lastNotNull"
              ],
              "fields": "",
              "values": false
            },
            "textMode": "auto"
          },
          "pluginVersion": "9.0.4",
          "targets": [
            {
              "datasource": {
                "type": "prometheus",
                "uid": "000000003"
              },
              "exemplar": true,
              "expr": "1 - avg(rate(node_cpu_seconds_total{mode=\"idle\",cluster=~\"$cluster\"}[$__rate_interval]))",
              "format": "time_series",
              "instant": false,
              "interval": "",
              "intervalFactor": 2,
              "legendFormat": "$cluster",
              "refId": "A"
            }
          ],
          "title": "Processor",
          "type": "stat"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "000000003"
          },
          "description": "",
          "fieldConfig": {
            "defaults": {
              "color": {
                "mode": "thresholds"
              },
              "decimals": 0,
              "mappings": [],
              "thresholds": {
                "mode": "absolute",
                "steps": [
                  {
                    "color": "green"
                  },
                  {
                    "color": "red",
                    "value": 80
                  }
                ]
              },
              "unit": "percentunit"
            },
            "overrides": []
          },
          "gridPos": {
            "h": 4,
            "w": 3,
            "x": 13,
            "y": 5
          },
          "id": 413,
          "links": [],
          "options": {
            "colorMode": "value",
            "graphMode": "area",
            "justifyMode": "auto",
            "orientation": "auto",
            "reduceOptions": {
              "calcs": [
                "lastNotNull"
              ],
              "fields": "",
              "values": false
            },
            "textMode": "auto"
          },
          "pluginVersion": "9.0.4",
          "targets": [
            {
              "datasource": {
                "type": "prometheus",
                "uid": "000000003"
              },
              "exemplar": true,
              "expr": "1 - sum(node_memory_MemAvailable_bytes{cluster=~\"$cluster\"}) / sum(node_memory_MemTotal_bytes{cluster=~\"$cluster\"})",
              "format": "time_series",
              "instant": false,
              "interval": "",
              "intervalFactor": 2,
              "legendFormat": "$cluster",
              "refId": "A"
            }
          ],
          "title": "Memory",
          "type": "stat"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "000000003"
          },
          "fieldConfig": {
            "defaults": {
              "color": {
                "mode": "thresholds"
              },
              "mappings": [],
              "thresholds": {
                "mode": "absolute",
                "steps": [
                  {
                    "color": "green"
                  },
                  {
                    "color": "red",
                    "value": 80
                  }
                ]
              }
            },
            "overrides": []
          },
          "gridPos": {
            "h": 4,
            "w": 3,
            "x": 16,
            "y": 5
          },
          "id": 370,
          "interval": "10m",
          "options": {
            "colorMode": "value",
            "graphMode": "area",
            "justifyMode": "auto",
            "orientation": "auto",
            "reduceOptions": {
              "calcs": [
                "mean"
              ],
              "fields": "",
              "values": false
            },
            "textMode": "auto"
          },
          "pluginVersion": "9.0.4",
          "targets": [
            {
              "datasource": {
                "type": "prometheus",
                "uid": "000000003"
              },
              "exemplar": true,
              "expr": "ceil(sum (rate(container_fs_reads_total{cluster=~\"$cluster\"}[5m]) + rate(container_fs_writes_total{cluster=~\"$cluster\"}[$__rate_interval])))",
              "interval": "",
              "legendFormat": "IOPS",
              "refId": "A"
            }
          ],
          "title": "#IOPS",
          "type": "stat"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "000000003"
          },
          "fieldConfig": {
            "defaults": {
              "color": {
                "mode": "thresholds"
              },
              "mappings": [],
              "thresholds": {
                "mode": "absolute",
                "steps": [
                  {
                    "color": "green"
                  },
                  {
                    "color": "red",
                    "value": 80
                  }
                ]
              },
              "unit": "Bps"
            },
            "overrides": []
          },
          "gridPos": {
            "h": 4,
            "w": 5,
            "x": 19,
            "y": 5
          },
          "id": 371,
          "interval": "10m",
          "options": {
            "colorMode": "value",
            "graphMode": "area",
            "justifyMode": "auto",
            "orientation": "auto",
            "reduceOptions": {
              "calcs": [
                "mean"
              ],
              "fields": "",
              "values": false
            },
            "textMode": "auto"
          },
          "pluginVersion": "9.0.4",
          "targets": [
            {
              "datasource": {
                "type": "prometheus",
                "uid": "000000003"
              },
              "exemplar": true,
              "expr": "sum(irate(container_network_receive_packets_total{cluster=~\"$cluster\", namespace=~\".+\"}[$__rate_interval])) ",
              "interval": "",
              "legendFormat": "ingress",
              "refId": "A"
            },
            {
              "datasource": {
                "type": "prometheus",
                "uid": "000000003"
              },
              "exemplar": true,
              "expr": "sum(irate(container_network_transmit_packets_total{cluster=\"$cluster\", namespace=~\".+\"}[$__rate_interval])) ",
              "hide": false,
              "interval": "",
              "legendFormat": "egress",
              "refId": "B"
            }
          ],
          "title": "Rate of Rx/Tx Packets",
          "type": "stat"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "000000003"
          },
          "fieldConfig": {
            "defaults": {
              "color": {
                "mode": "thresholds"
              },
              "mappings": [],
              "noValue": "PVC not Claimed/Bound",
              "thresholds": {
                "mode": "percentage",
                "steps": [
                  {
                    "color": "green"
                  },
                  {
                    "color": "#EAB839",
                    "value": 90
                  }
                ]
              },
              "unit": "decbytes"
            },
            "overrides": []
          },
          "gridPos": {
            "h": 6,
            "w": 3,
            "x": 0,
            "y": 9
          },
          "id": 488,
          "links": [],
          "options": {
            "displayMode": "gradient",
            "minVizHeight": 10,
            "minVizWidth": 0,
            "orientation": "auto",
            "reduceOptions": {
              "calcs": [],
              "fields": "",
              "values": false
            },
            "showUnfilled": true,
            "text": {
              "titleSize": 11,
              "valueSize": 15
            }
          },
          "pluginVersion": "9.0.4",
          "targets": [
            {
              "datasource": {
                "type": "prometheus",
                "uid": "000000003"
              },
              "exemplar": true,
              "expr": "sum by (cluster) (kubelet_volume_stats_capacity_bytes{cluster=~\"$cluster\"})",
              "interval": "",
              "intervalFactor": 1,
              "legendFormat": "Total",
              "refId": "B"
            },
            {
              "datasource": {
                "type": "prometheus",
                "uid": "000000003"
              },
              "exemplar": true,
              "expr": "sum by (cluster) (kubelet_volume_stats_available_bytes{cluster=~\"$cluster\"})",
              "hide": false,
              "interval": "",
              "intervalFactor": 1,
              "legendFormat": "Available",
              "refId": "C"
            },
            {
              "datasource": {
                "type": "prometheus",
                "uid": "000000003"
              },
              "exemplar": true,
              "expr": "sum by (cluster) (kubelet_volume_stats_used_bytes{cluster=~\"$cluster\"})",
              "hide": false,
              "interval": "",
              "legendFormat": "Utilized",
              "refId": "A"
            }
          ],
          "title": "#PVC storage",
          "type": "bargauge"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "000000003"
          },
          "fieldConfig": {
            "defaults": {
              "color": {
                "mode": "palette-classic"
              },
              "custom": {
                "axisLabel": "",
                "axisPlacement": "auto",
                "barAlignment": 0,
                "drawStyle": "line",
                "fillOpacity": 0,
                "gradientMode": "none",
                "hideFrom": {
                  "legend": false,
                  "tooltip": false,
                  "viz": false
                },
                "lineInterpolation": "linear",
                "lineWidth": 1,
                "pointSize": 5,
                "scaleDistribution": {
                  "type": "linear"
                },
                "showPoints": "auto",
                "spanNulls": true,
                "stacking": {
                  "group": "A",
                  "mode": "none"
                },
                "thresholdsStyle": {
                  "mode": "off"
                }
              },
              "mappings": [],
              "thresholds": {
                "mode": "absolute",
                "steps": [
                  {
                    "color": "green"
                  },
                  {
                    "color": "red",
                    "value": 80
                  }
                ]
              },
              "unit": "percentunit"
            },
            "overrides": []
          },
          "gridPos": {
            "h": 6,
            "w": 7,
            "x": 3,
            "y": 9
          },
          "id": 326,
          "interval": "1m",
          "links": [],
          "options": {
            "legend": {
              "calcs": [],
              "displayMode": "list",
              "placement": "bottom"
            },
            "tooltip": {
              "mode": "single",
              "sort": "none"
            }
          },
          "pluginVersion": "8.3.2",
          "targets": [
            {
              "datasource": {
                "type": "prometheus",
                "uid": "000000003"
              },
              "exemplar": true,
              "expr": "1 - avg(rate(node_cpu_seconds_total{mode=\"idle\",cluster=~\"$cluster\"}[$__rate_interval]))",
              "format": "time_series",
              "instant": false,
              "interval": "",
              "intervalFactor": 2,
              "legendFormat": "$cluster",
              "refId": "A"
            }
          ],
          "title": "Processor utilization ",
          "type": "timeseries"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "000000003"
          },
          "fieldConfig": {
            "defaults": {
              "color": {
                "mode": "palette-classic"
              },
              "custom": {
                "axisLabel": "",
                "axisPlacement": "auto",
                "barAlignment": 0,
                "drawStyle": "line",
                "fillOpacity": 0,
                "gradientMode": "none",
                "hideFrom": {
                  "legend": false,
                  "tooltip": false,
                  "viz": false
                },
                "lineInterpolation": "linear",
                "lineWidth": 1,
                "pointSize": 5,
                "scaleDistribution": {
                  "type": "linear"
                },
                "showPoints": "auto",
                "spanNulls": true,
                "stacking": {
                  "group": "A",
                  "mode": "none"
                },
                "thresholdsStyle": {
                  "mode": "off"
                }
              },
              "mappings": [],
              "thresholds": {
                "mode": "absolute",
                "steps": [
                  {
                    "color": "green"
                  },
                  {
                    "color": "red",
                    "value": 80
                  }
                ]
              },
              "unit": "percentunit"
            },
            "overrides": []
          },
          "gridPos": {
            "h": 6,
            "w": 7,
            "x": 10,
            "y": 9
          },
          "id": 328,
          "links": [],
          "options": {
            "legend": {
              "calcs": [],
              "displayMode": "list",
              "placement": "bottom"
            },
            "tooltip": {
              "mode": "single",
              "sort": "none"
            }
          },
          "pluginVersion": "8.3.2",
          "targets": [
            {
              "datasource": {
                "type": "prometheus",
                "uid": "000000003"
              },
              "exemplar": true,
              "expr": "1 - sum(node_memory_MemAvailable_bytes{cluster=~\"$cluster\"}) / sum(node_memory_MemTotal_bytes{cluster=~\"$cluster\"})",
              "format": "time_series",
              "instant": false,
              "interval": "",
              "intervalFactor": 2,
              "legendFormat": "$cluster",
              "refId": "A"
            }
          ],
          "title": "memory utilization ",
          "type": "timeseries"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "000000003"
          },
          "fieldConfig": {
            "defaults": {
              "color": {
                "mode": "palette-classic"
              },
              "custom": {
                "axisLabel": "",
                "axisPlacement": "auto",
                "barAlignment": 0,
                "drawStyle": "line",
                "fillOpacity": 4,
                "gradientMode": "none",
                "hideFrom": {
                  "legend": false,
                  "tooltip": false,
                  "viz": false
                },
                "lineInterpolation": "linear",
                "lineWidth": 1,
                "pointSize": 5,
                "scaleDistribution": {
                  "type": "linear"
                },
                "showPoints": "auto",
                "spanNulls": true,
                "stacking": {
                  "group": "A",
                  "mode": "none"
                },
                "thresholdsStyle": {
                  "mode": "off"
                }
              },
              "mappings": [],
              "thresholds": {
                "mode": "absolute",
                "steps": [
                  {
                    "color": "green"
                  },
                  {
                    "color": "red",
                    "value": 80
                  }
                ]
              },
              "unit": "Bps"
            },
            "overrides": []
          },
          "gridPos": {
            "h": 6,
            "w": 7,
            "x": 17,
            "y": 9
          },
          "id": 194,
          "interval": "10m",
          "options": {
            "legend": {
              "calcs": [],
              "displayMode": "list",
              "placement": "bottom"
            },
            "tooltip": {
              "mode": "single",
              "sort": "none"
            }
          },
          "targets": [
            {
              "datasource": {
                "type": "prometheus",
                "uid": "000000003"
              },
              "exemplar": true,
              "expr": "sum(irate(container_network_receive_packets_total{cluster=~\"$cluster\", namespace=~\".+\"}[$__rate_interval])) ",
              "interval": "",
              "legendFormat": "ingress",
              "refId": "A"
            },
            {
              "datasource": {
                "type": "prometheus",
                "uid": "000000003"
              },
              "exemplar": true,
              "expr": "sum(irate(container_network_transmit_packets_total{cluster=\"$cluster\", namespace=~\".+\"}[$__rate_interval])) ",
              "hide": false,
              "interval": "",
              "legendFormat": "egress",
              "refId": "B"
            }
          ],
          "title": "Network - Received vs Transmitted kB/s",
          "type": "timeseries"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "000000003"
          },
          "fieldConfig": {
            "defaults": {
              "color": {
                "mode": "palette-classic"
              },
              "custom": {
                "axisLabel": "",
                "axisPlacement": "auto",
                "barAlignment": 0,
                "drawStyle": "line",
                "fillOpacity": 5,
                "gradientMode": "none",
                "hideFrom": {
                  "legend": false,
                  "tooltip": false,
                  "viz": false
                },
                "lineInterpolation": "linear",
                "lineWidth": 1,
                "pointSize": 5,
                "scaleDistribution": {
                  "type": "linear"
                },
                "showPoints": "auto",
                "spanNulls": true,
                "stacking": {
                  "group": "A",
                  "mode": "none"
                },
                "thresholdsStyle": {
                  "mode": "off"
                }
              },
              "mappings": [],
              "thresholds": {
                "mode": "absolute",
                "steps": [
                  {
                    "color": "green"
                  },
                  {
                    "color": "red",
                    "value": 80
                  }
                ]
              }
            },
            "overrides": []
          },
          "gridPos": {
            "h": 7,
            "w": 12,
            "x": 0,
            "y": 15
          },
          "id": 196,
          "interval": "10m",
          "options": {
            "legend": {
              "calcs": [],
              "displayMode": "list",
              "placement": "bottom"
            },
            "tooltip": {
              "mode": "single",
              "sort": "none"
            }
          },
          "targets": [
            {
              "datasource": {
                "type": "prometheus",
                "uid": "000000003"
              },
              "exemplar": true,
              "expr": "ceil(sum (rate(container_fs_reads_total{cluster=~\"$cluster\"}[$__rate_interval])))   ",
              "interval": "",
              "legendFormat": "#Reads",
              "refId": "A"
            },
            {
              "datasource": {
                "type": "prometheus",
                "uid": "000000003"
              },
              "exemplar": true,
              "expr": "ceil(sum (rate(container_fs_writes_total{cluster=~\"$cluster\"}[$__rate_interval])))",
              "hide": false,
              "interval": "",
              "legendFormat": "#Writes",
              "refId": "B"
            }
          ],
          "title": "Storage - IOPS",
          "type": "timeseries"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "000000003"
          },
          "fieldConfig": {
            "defaults": {
              "color": {
                "mode": "palette-classic"
              },
              "custom": {
                "axisLabel": "",
                "axisPlacement": "auto",
                "barAlignment": 0,
                "drawStyle": "line",
                "fillOpacity": 2,
                "gradientMode": "none",
                "hideFrom": {
                  "legend": false,
                  "tooltip": false,
                  "viz": false
                },
                "lineInterpolation": "linear",
                "lineStyle": {
                  "fill": "solid"
                },
                "lineWidth": 1,
                "pointSize": 5,
                "scaleDistribution": {
                  "type": "linear"
                },
                "showPoints": "auto",
                "spanNulls": true,
                "stacking": {
                  "group": "A",
                  "mode": "none"
                },
                "thresholdsStyle": {
                  "mode": "off"
                }
              },
              "mappings": [],
              "min": 0,
              "thresholds": {
                "mode": "absolute",
                "steps": [
                  {
                    "color": "green"
                  },
                  {
                    "color": "red",
                    "value": 80
                  }
                ]
              },
              "unit": "Bps"
            },
            "overrides": []
          },
          "gridPos": {
            "h": 7,
            "w": 12,
            "x": 12,
            "y": 15
          },
          "id": 411,
          "interval": "30s",
          "links": [],
          "options": {
            "legend": {
              "calcs": [],
              "displayMode": "list",
              "placement": "bottom"
            },
            "tooltip": {
              "mode": "single",
              "sort": "none"
            }
          },
          "pluginVersion": "8.3.2",
          "targets": [
            {
              "datasource": {
                "type": "prometheus",
                "uid": "000000003"
              },
              "exemplar": true,
              "expr": "ceil(sum (rate(container_fs_reads_bytes_total{cluster=~\"$cluster\"}[$__rate_interval])))",
              "format": "time_series",
              "interval": "",
              "intervalFactor": 1,
              "legendFormat": "Read MB/s",
              "refId": "A",
              "step": 10
            },
            {
              "datasource": {
                "type": "prometheus",
                "uid": "000000003"
              },
              "exemplar": true,
              "expr": "ceil(sum (rate(container_fs_writes_bytes_total{cluster=~\"$cluster\"}[$__rate_interval])))",
              "hide": false,
              "interval": "",
              "intervalFactor": 1,
              "legendFormat": "Write MB/s",
              "refId": "B"
            }
          ],
          "title": "Storage - throughput MB/s",
          "type": "timeseries"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "000000003"
          },
          "fieldConfig": {
            "defaults": {
              "color": {
                "mode": "palette-classic"
              },
              "custom": {
                "axisLabel": "",
                "axisPlacement": "auto",
                "barAlignment": 0,
                "drawStyle": "line",
                "fillOpacity": 0,
                "gradientMode": "none",
                "hideFrom": {
                  "legend": false,
                  "tooltip": false,
                  "viz": false
                },
                "lineInterpolation": "linear",
                "lineWidth": 1,
                "pointSize": 5,
                "scaleDistribution": {
                  "type": "linear"
                },
                "showPoints": "never",
                "spanNulls": true,
                "stacking": {
                  "group": "A",
                  "mode": "none"
                },
                "thresholdsStyle": {
                  "mode": "off"
                }
              },
              "mappings": [],
              "thresholds": {
                "mode": "absolute",
                "steps": [
                  {
                    "color": "green"
                  },
                  {
                    "color": "red",
                    "value": 80
                  }
                ]
              },
              "unit": "decbytes"
            },
            "overrides": []
          },
          "gridPos": {
            "h": 6,
            "w": 12,
            "x": 0,
            "y": 22
          },
          "id": 427,
          "options": {
            "legend": {
              "calcs": [
                "mean",
                "lastNotNull",
                "max",
                "min"
              ],
              "displayMode": "table",
              "placement": "right"
            },
            "tooltip": {
              "mode": "single",
              "sort": "none"
            }
          },
          "pluginVersion": "8.3.2",
          "targets": [
            {
              "datasource": {
                "type": "prometheus",
                "uid": "000000003"
              },
              "exemplar": true,
              "expr": "(max by (persistentvolumeclaim,namespace) (kubelet_volume_stats_used_bytes{cluster=~\"$cluster\"}))",
              "interval": "",
              "legendFormat": "{{namespace}} ({{persistentvolumeclaim}})",
              "refId": "A"
            }
          ],
          "title": "All Running PVCs Used Bytes",
          "type": "timeseries"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "000000003"
          },
          "fieldConfig": {
            "defaults": {
              "color": {
                "mode": "palette-classic"
              },
              "custom": {
                "axisLabel": "",
                "axisPlacement": "auto",
                "barAlignment": 0,
                "drawStyle": "line",
                "fillOpacity": 0,
                "gradientMode": "none",
                "hideFrom": {
                  "legend": false,
                  "tooltip": false,
                  "viz": false
                },
                "lineInterpolation": "linear",
                "lineWidth": 1,
                "pointSize": 5,
                "scaleDistribution": {
                  "type": "linear"
                },
                "showPoints": "never",
                "spanNulls": true,
                "stacking": {
                  "group": "A",
                  "mode": "none"
                },
                "thresholdsStyle": {
                  "mode": "off"
                }
              },
              "mappings": [],
              "thresholds": {
                "mode": "absolute",
                "steps": [
                  {
                    "color": "green"
                  },
                  {
                    "color": "red",
                    "value": 80
                  }
                ]
              },
              "unit": "binBps"
            },
            "overrides": []
          },
          "gridPos": {
            "h": 6,
            "w": 12,
            "x": 12,
            "y": 22
          },
          "id": 441,
          "options": {
            "legend": {
              "calcs": [
                "mean"
              ],
              "displayMode": "table",
              "placement": "right"
            },
            "tooltip": {
              "mode": "single",
              "sort": "none"
            }
          },
          "pluginVersion": "8.3.2",
          "targets": [
            {
              "datasource": {
                "type": "prometheus",
                "uid": "000000003"
              },
              "exemplar": true,
              "expr": "rate(kubelet_volume_stats_used_bytes{cluster=~\"$cluster\"}[1d])",
              "interval": "",
              "legendFormat": "{{namespace}} ({{persistentvolumeclaim}})",
              "refId": "A"
            }
          ],
          "title": "PVC Daily Usage Rate",
          "type": "timeseries"
        }
      ],
      "targets": [
        {
          "datasource": {
            "type": "prometheus",
            "uid": "000000003"
          },
          "refId": "A"
        }
      ],
      "title": "Cluster",
      "type": "row"
    },
    {
      "collapsed": true,
      "datasource": {
        "type": "prometheus",
        "uid": "000000003"
      },
      "gridPos": {
        "h": 1,
        "w": 24,
        "x": 0,
        "y": 5
      },
      "id": 14,
      "panels": [
        {
          "datasource": {
            "type": "prometheus",
            "uid": "000000003"
          },
          "description": "Busy state of all CPU cores together",
          "fieldConfig": {
            "defaults": {
              "color": {
                "mode": "palette-classic"
              },
              "custom": {
                "axisLabel": "",
                "axisPlacement": "auto",
                "barAlignment": 0,
                "drawStyle": "line",
                "fillOpacity": 0,
                "gradientMode": "none",
                "hideFrom": {
                  "legend": false,
                  "tooltip": false,
                  "viz": false
                },
                "lineInterpolation": "linear",
                "lineWidth": 1,
                "pointSize": 5,
                "scaleDistribution": {
                  "type": "linear"
                },
                "showPoints": "auto",
                "spanNulls": false,
                "stacking": {
                  "group": "A",
                  "mode": "none"
                },
                "thresholdsStyle": {
                  "mode": "off"
                }
              },
              "mappings": [
                {
                  "options": {
                    "null": {
                      "index": 0,
                      "text": "na"
                    }
                  },
                  "type": "value"
                }
              ],
              "min": 0,
              "thresholds": {
                "mode": "absolute",
                "steps": [
                  {
                    "color": "dark-green"
                  },
                  {
                    "color": "#EAB839",
                    "value": 70
                  },
                  {
                    "color": "dark-orange",
                    "value": 80
                  },
                  {
                    "color": "dark-red",
                    "value": 90
                  }
                ]
              },
              "unit": "percent"
            },
            "overrides": []
          },
          "gridPos": {
            "h": 8,
            "w": 12,
            "x": 0,
            "y": 2
          },
          "id": 27,
          "options": {
            "legend": {
              "calcs": [
                "lastNotNull"
              ],
              "displayMode": "list",
              "placement": "bottom"
            },
            "tooltip": {
              "mode": "single",
              "sort": "none"
            }
          },
          "pluginVersion": "8.3.2",
          "targets": [
            {
              "datasource": {
                "type": "prometheus",
                "uid": "000000003"
              },
              "exemplar": true,
              "expr": "100 - (avg by (node) (rate(node_cpu_seconds_total{component=\"node-exporter\",mode=\"idle\",node=~\"$node\"}[15m])) * 100)",
              "hide": false,
              "interval": "",
              "intervalFactor": 1,
              "legendFormat": "{{node}}",
              "refId": "A"
            },
            {
              "alias": "",
              "bucketAggs": [
                {
                  "field": "startTime",
                  "id": "2",
                  "settings": {
                    "interval": "auto"
                  },
                  "type": "date_histogram"
                }
              ],
              "datasource": {
                "type": "prometheus",
                "uid": "000000003"
              },
              "exemplar": true,
              "expr": "(((count(count(node_cpu_seconds_total{node=~\"$node\",job=~\"$job\"}) by (cpu))) - avg(sum by (mode)(rate(node_cpu_seconds_total{mode='idle',node=~\"$node\",job=~\"$job\"}[$__rate_interval])))) * 100) / count(count(node_cpu_seconds_total{node=~\"$node\",job=~\"$job\"}) by (cpu))",
              "hide": true,
              "interval": "",
              "legendFormat": "",
              "metrics": [
                {
                  "id": "1",
                  "type": "count"
                }
              ],
              "query": "",
              "refId": "B",
              "timeField": "startTime"
            }
          ],
          "title": "Processor utilization ",
          "transformations": [],
          "type": "timeseries"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "000000003"
          },
          "fieldConfig": {
            "defaults": {
              "color": {
                "mode": "palette-classic"
              },
              "custom": {
                "axisLabel": "",
                "axisPlacement": "auto",
                "barAlignment": 0,
                "drawStyle": "line",
                "fillOpacity": 0,
                "gradientMode": "none",
                "hideFrom": {
                  "legend": false,
                  "tooltip": false,
                  "viz": false
                },
                "lineInterpolation": "linear",
                "lineWidth": 1,
                "pointSize": 5,
                "scaleDistribution": {
                  "type": "linear"
                },
                "showPoints": "auto",
                "spanNulls": false,
                "stacking": {
                  "group": "A",
                  "mode": "none"
                },
                "thresholdsStyle": {
                  "mode": "off"
                }
              },
              "decimals": 0,
              "mappings": [],
              "thresholds": {
                "mode": "absolute",
                "steps": [
                  {
                    "color": "dark-green"
                  },
                  {
                    "color": "#EAB839",
                    "value": 70
                  },
                  {
                    "color": "dark-orange",
                    "value": 80
                  },
                  {
                    "color": "dark-red",
                    "value": 90
                  }
                ]
              },
              "unit": "percent"
            },
            "overrides": []
          },
          "gridPos": {
            "h": 8,
            "w": 12,
            "x": 12,
            "y": 2
          },
          "id": 46,
          "options": {
            "legend": {
              "calcs": [
                "lastNotNull"
              ],
              "displayMode": "list",
              "placement": "bottom"
            },
            "tooltip": {
              "mode": "single",
              "sort": "none"
            }
          },
          "pluginVersion": "8.3.2",
          "targets": [
            {
              "datasource": {
                "type": "prometheus",
                "uid": "000000003"
              },
              "exemplar": true,
              "expr": "100 - ((avg by (node) (node_memory_MemAvailable_bytes{node=~\"$node\",job=~\"$job\"}) * 100)) /(avg by (node) (node_memory_MemTotal_bytes{node=~\"$node\",job=~\"$job\"}))",
              "interval": "",
              "legendFormat": "{{node}}",
              "refId": "A"
            }
          ],
          "title": "Memory utilization - Trend",
          "transformations": [
            {
              "id": "renameByRegex",
              "options": {
                "regex": "(:9100)",
                "renamePattern": ""
              }
            }
          ],
          "type": "timeseries"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "000000003"
          },
          "description": "",
          "fieldConfig": {
            "defaults": {
              "color": {
                "mode": "palette-classic"
              },
              "custom": {
                "axisLabel": "",
                "axisPlacement": "auto",
                "barAlignment": 0,
                "drawStyle": "line",
                "fillOpacity": 0,
                "gradientMode": "none",
                "hideFrom": {
                  "legend": false,
                  "tooltip": false,
                  "viz": false
                },
                "lineInterpolation": "linear",
                "lineWidth": 1,
                "pointSize": 5,
                "scaleDistribution": {
                  "type": "linear"
                },
                "showPoints": "auto",
                "spanNulls": true,
                "stacking": {
                  "group": "A",
                  "mode": "none"
                },
                "thresholdsStyle": {
                  "mode": "off"
                }
              },
              "mappings": [
                {
                  "options": {
                    "null": {
                      "index": 0,
                      "text": "na"
                    }
                  },
                  "type": "value"
                }
              ],
              "min": 0,
              "thresholds": {
                "mode": "absolute",
                "steps": [
                  {
                    "color": "dark-green"
                  },
                  {
                    "color": "#EAB839",
                    "value": 70
                  },
                  {
                    "color": "dark-orange",
                    "value": 80
                  },
                  {
                    "color": "dark-red",
                    "value": 90
                  }
                ]
              },
              "unit": "none"
            },
            "overrides": []
          },
          "gridPos": {
            "h": 6,
            "w": 24,
            "x": 0,
            "y": 10
          },
          "id": 522,
          "options": {
            "legend": {
              "calcs": [
                "lastNotNull",
                "mean"
              ],
              "displayMode": "list",
              "placement": "bottom"
            },
            "tooltip": {
              "mode": "single",
              "sort": "none"
            }
          },
          "pluginVersion": "8.3.2",
          "targets": [
            {
              "datasource": {
                "type": "prometheus",
                "uid": "000000003"
              },
              "exemplar": true,
              "expr": "ceil(sum (rate(container_fs_reads_total{cluster=~\"$cluster\",node=~\"$node\"}[5m]) + rate(container_fs_writes_total{cluster=~\"$cluster\",node=~\"$node\"}[$__rate_interval])) by (node))",
              "hide": false,
              "interval": "",
              "intervalFactor": 1,
              "legendFormat": "{{node}}",
              "refId": "B"
            }
          ],
          "title": "Node IOPS",
          "transformations": [],
          "type": "timeseries"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "000000003"
          },
          "description": "Disk space used of all filesystems mounted",
          "fieldConfig": {
            "defaults": {
              "color": {
                "mode": "palette-classic"
              },
              "custom": {
                "axisLabel": "",
                "axisPlacement": "auto",
                "barAlignment": 0,
                "drawStyle": "line",
                "fillOpacity": 28,
                "gradientMode": "none",
                "hideFrom": {
                  "legend": false,
                  "tooltip": false,
                  "viz": false
                },
                "lineInterpolation": "linear",
                "lineStyle": {
                  "fill": "solid"
                },
                "lineWidth": 1,
                "pointSize": 5,
                "scaleDistribution": {
                  "type": "linear"
                },
                "showPoints": "never",
                "spanNulls": true,
                "stacking": {
                  "group": "A",
                  "mode": "none"
                },
                "thresholdsStyle": {
                  "mode": "off"
                }
              },
              "mappings": [],
              "max": 100,
              "min": 0,
              "thresholds": {
                "mode": "absolute",
                "steps": [
                  {
                    "color": "green"
                  },
                  {
                    "color": "red",
                    "value": 80
                  }
                ]
              },
              "unit": "percent"
            },
            "overrides": [
              {
                "matcher": {
                  "id": "byName",
                  "options": "/run"
                },
                "properties": [
                  {
                    "id": "color",
                    "value": {
                      "fixedColor": "dark-blue",
                      "mode": "fixed"
                    }
                  }
                ]
              },
              {
                "matcher": {
                  "id": "byName",
                  "options": "/run/user/501"
                },
                "properties": [
                  {
                    "id": "color",
                    "value": {
                      "fixedColor": "dark-orange",
                      "mode": "fixed"
                    }
                  }
                ]
              },
              {
                "matcher": {
                  "id": "byName",
                  "options": "/"
                },
                "properties": [
                  {
                    "id": "color",
                    "value": {
                      "fixedColor": "dark-green",
                      "mode": "fixed"
                    }
                  }
                ]
              }
            ]
          },
          "gridPos": {
            "h": 5,
            "w": 12,
            "x": 0,
            "y": 16
          },
          "id": 79,
          "options": {
            "legend": {
              "calcs": [
                "lastNotNull"
              ],
              "displayMode": "list",
              "placement": "bottom"
            },
            "tooltip": {
              "mode": "single",
              "sort": "none"
            }
          },
          "repeat": "node",
          "repeatDirection": "v",
          "targets": [
            {
              "datasource": {
                "type": "prometheus",
                "uid": "000000003"
              },
              "exemplar": true,
              "expr": "100 - ((node_filesystem_avail_bytes{node=~\"$node\",job=~\"$job\"} * 100) / node_filesystem_size_bytes{node=~\"$node\",job=~\"$job\"})",
              "interval": "",
              "legendFormat": "$node: {{mountpoint}}",
              "refId": "A"
            }
          ],
          "title": "FS space utilization in % - Trend",
          "transformations": [
            {
              "id": "renameByRegex",
              "options": {
                "regex": "(:9100)",
                "renamePattern": ""
              }
            }
          ],
          "type": "timeseries"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "000000003"
          },
          "description": "Disk space used of all filesystems mounted",
          "fieldConfig": {
            "defaults": {
              "color": {
                "mode": "palette-classic"
              },
              "custom": {
                "axisLabel": "",
                "axisPlacement": "auto",
                "barAlignment": 0,
                "drawStyle": "line",
                "fillOpacity": 28,
                "gradientMode": "none",
                "hideFrom": {
                  "legend": false,
                  "tooltip": false,
                  "viz": false
                },
                "lineInterpolation": "linear",
                "lineStyle": {
                  "fill": "solid"
                },
                "lineWidth": 1,
                "pointSize": 5,
                "scaleDistribution": {
                  "type": "linear"
                },
                "showPoints": "never",
                "spanNulls": true,
                "stacking": {
                  "group": "A",
                  "mode": "none"
                },
                "thresholdsStyle": {
                  "mode": "off"
                }
              },
              "mappings": [],
              "min": 0,
              "thresholds": {
                "mode": "absolute",
                "steps": [
                  {
                    "color": "green"
                  },
                  {
                    "color": "red",
                    "value": 80
                  }
                ]
              },
              "unit": "decbytes"
            },
            "overrides": []
          },
          "gridPos": {
            "h": 5,
            "w": 12,
            "x": 12,
            "y": 16
          },
          "id": 78,
          "options": {
            "legend": {
              "calcs": [
                "lastNotNull"
              ],
              "displayMode": "list",
              "placement": "bottom"
            },
            "tooltip": {
              "mode": "single",
              "sort": "none"
            }
          },
          "repeat": "node",
          "repeatDirection": "v",
          "targets": [
            {
              "datasource": {
                "type": "prometheus",
                "uid": "000000003"
              },
              "exemplar": true,
              "expr": "(node_filesystem_size_bytes{node=~\"$node\",mountpoint=~\".*\"} - node_filesystem_avail_bytes{node=~\"$node\", mountpoint=~\".*\"})",
              "instant": false,
              "interval": "",
              "legendFormat": "$node: {{mountpoint}}",
              "refId": "A"
            }
          ],
          "title": "FS space utilization in GB - Trend",
          "transformations": [
            {
              "id": "renameByRegex",
              "options": {
                "regex": "(:9100)",
                "renamePattern": ""
              }
            }
          ],
          "type": "timeseries"
        }
      ],
      "targets": [
        {
          "datasource": {
            "type": "prometheus",
            "uid": "000000003"
          },
          "refId": "A"
        }
      ],
      "title": "Node",
      "type": "row"
    },
    {
      "collapsed": true,
      "datasource": {
        "type": "prometheus",
        "uid": "000000003"
      },
      "gridPos": {
        "h": 1,
        "w": 24,
        "x": 0,
        "y": 6
      },
      "id": 373,
      "panels": [
        {
          "datasource": {
            "type": "prometheus",
            "uid": "${cluster}"
          },
          "fieldConfig": {
            "defaults": {
              "color": {
                "mode": "thresholds"
              },
              "mappings": [],
              "thresholds": {
                "mode": "absolute",
                "steps": [
                  {
                    "color": "green"
                  },
                  {
                    "color": "red",
                    "value": 80
                  }
                ]
              }
            },
            "overrides": []
          },
          "gridPos": {
            "h": 4,
            "w": 2,
            "x": 0,
            "y": 7
          },
          "id": 469,
          "options": {
            "colorMode": "none",
            "graphMode": "none",
            "justifyMode": "center",
            "orientation": "auto",
            "reduceOptions": {
              "calcs": [
                "lastNotNull"
              ],
              "fields": "",
              "values": false
            },
            "textMode": "value"
          },
          "pluginVersion": "9.0.4",
          "targets": [
            {
              "datasource": {
                "type": "prometheus",
                "uid": "${cluster}"
              },
              "exemplar": true,
              "expr": "count by (namespace) (namespace_workload_pod:kube_pod_owner:relabel{cluster=~\"sj-ci-cluster1\",namespace=~\"$namespace\"})",
              "interval": "",
              "legendFormat": "",
              "refId": "A"
            }
          ],
          "title": "#Workloads",
          "type": "stat"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "000000003"
          },
          "fieldConfig": {
            "defaults": {
              "color": {
                "mode": "thresholds"
              },
              "mappings": [],
              "thresholds": {
                "mode": "absolute",
                "steps": [
                  {
                    "color": "green"
                  },
                  {
                    "color": "red",
                    "value": 80
                  }
                ]
              }
            },
            "overrides": []
          },
          "gridPos": {
            "h": 4,
            "w": 2,
            "x": 2,
            "y": 7
          },
          "id": 471,
          "options": {
            "colorMode": "none",
            "graphMode": "none",
            "justifyMode": "center",
            "orientation": "auto",
            "reduceOptions": {
              "calcs": [
                "lastNotNull"
              ],
              "fields": "",
              "values": false
            },
            "textMode": "value"
          },
          "pluginVersion": "9.0.4",
          "targets": [
            {
              "datasource": {
                "type": "prometheus",
                "uid": "000000003"
              },
              "exemplar": true,
              "expr": "count (kube_pod_info{cluster=~\"$cluster\",namespace=~\"$namespace\"})",
              "interval": "",
              "legendFormat": "",
              "refId": "A"
            }
          ],
          "title": "#Pods",
          "type": "stat"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "000000003"
          },
          "fieldConfig": {
            "defaults": {
              "color": {
                "mode": "thresholds"
              },
              "mappings": [],
              "thresholds": {
                "mode": "absolute",
                "steps": [
                  {
                    "color": "green"
                  },
                  {
                    "color": "red",
                    "value": 80
                  }
                ]
              }
            },
            "overrides": []
          },
          "gridPos": {
            "h": 4,
            "w": 2,
            "x": 4,
            "y": 7
          },
          "id": 470,
          "options": {
            "colorMode": "none",
            "graphMode": "none",
            "justifyMode": "center",
            "orientation": "auto",
            "reduceOptions": {
              "calcs": [
                "lastNotNull"
              ],
              "fields": "",
              "values": false
            },
            "textMode": "value"
          },
          "pluginVersion": "9.0.4",
          "targets": [
            {
              "datasource": {
                "type": "prometheus",
                "uid": "000000003"
              },
              "exemplar": true,
              "expr": "count(kube_pod_container_info{cluster=~\"$cluster\",namespace=~\"$namespace\"})",
              "interval": "",
              "legendFormat": "",
              "refId": "A"
            }
          ],
          "title": "#Containers",
          "type": "stat"
        },
        {
          "datasource": {},
          "fieldConfig": {
            "defaults": {
              "color": {
                "mode": "thresholds"
              },
              "mappings": [],
              "noValue": "0",
              "thresholds": {
                "mode": "absolute",
                "steps": [
                  {
                    "color": "green"
                  },
                  {
                    "color": "red",
                    "value": 80
                  }
                ]
              }
            },
            "overrides": []
          },
          "gridPos": {
            "h": 4,
            "w": 2,
            "x": 6,
            "y": 7
          },
          "id": 487,
          "options": {
            "colorMode": "none",
            "graphMode": "none",
            "justifyMode": "center",
            "orientation": "auto",
            "reduceOptions": {
              "calcs": [
                "last"
              ],
              "fields": "",
              "values": false
            },
            "textMode": "value"
          },
          "pluginVersion": "9.0.4",
          "targets": [
            {
              "datasource": {
                "type": "prometheus",
                "uid": "${cluster}"
              },
              "exemplar": true,
              "expr": "count (kube_persistentvolumeclaim_info{cluster=~\"$cluster\",namespace=\"$namespace\"})",
              "interval": "",
              "intervalFactor": 1,
              "legendFormat": "",
              "refId": "A"
            }
          ],
          "title": "#PVC",
          "type": "stat"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "000000003"
          },
          "fieldConfig": {
            "defaults": {
              "color": {
                "mode": "thresholds"
              },
              "mappings": [],
              "noValue": "PVC not Claimed/Bound",
              "thresholds": {
                "mode": "percentage",
                "steps": [
                  {
                    "color": "green"
                  },
                  {
                    "color": "#EAB839",
                    "value": 90
                  }
                ]
              },
              "unit": "decbytes"
            },
            "overrides": []
          },
          "gridPos": {
            "h": 4,
            "w": 7,
            "x": 8,
            "y": 7
          },
          "id": 505,
          "links": [],
          "options": {
            "displayMode": "gradient",
            "minVizHeight": 10,
            "minVizWidth": 0,
            "orientation": "auto",
            "reduceOptions": {
              "calcs": [],
              "fields": "",
              "values": false
            },
            "showUnfilled": true
          },
          "pluginVersion": "9.0.4",
          "targets": [
            {
              "datasource": {
                "type": "prometheus",
                "uid": "000000003"
              },
              "exemplar": true,
              "expr": "sum by (cluster) (kubelet_volume_stats_capacity_bytes{cluster=~\"$cluster\",namespace=\"$namespace\"})",
              "interval": "",
              "intervalFactor": 1,
              "legendFormat": "Total",
              "refId": "B"
            },
            {
              "datasource": {
                "type": "prometheus",
                "uid": "000000003"
              },
              "exemplar": true,
              "expr": "sum by (cluster) (kubelet_volume_stats_available_bytes{cluster=~\"$cluster\",namespace=\"$namespace\"})",
              "hide": false,
              "interval": "",
              "intervalFactor": 1,
              "legendFormat": "Available",
              "refId": "C"
            },
            {
              "datasource": {
                "type": "prometheus",
                "uid": "000000003"
              },
              "exemplar": true,
              "expr": "sum by (cluster) (kubelet_volume_stats_used_bytes{cluster=~\"$cluster\",namespace=\"$namespace\"})",
              "hide": false,
              "interval": "",
              "legendFormat": "Utilized",
              "refId": "A"
            }
          ],
          "title": "#PVC storage",
          "type": "bargauge"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "000000003"
          },
          "fieldConfig": {
            "defaults": {
              "color": {
                "mode": "thresholds"
              },
              "mappings": [],
              "min": 0,
              "thresholds": {
                "mode": "absolute",
                "steps": [
                  {
                    "color": "green"
                  }
                ]
              },
              "unit": "decbytes"
            },
            "overrides": []
          },
          "gridPos": {
            "h": 4,
            "w": 3,
            "x": 15,
            "y": 7
          },
          "id": 332,
          "links": [],
          "options": {
            "colorMode": "value",
            "graphMode": "area",
            "justifyMode": "auto",
            "orientation": "auto",
            "reduceOptions": {
              "calcs": [
                "lastNotNull"
              ],
              "fields": "",
              "values": false
            },
            "textMode": "auto"
          },
          "pluginVersion": "9.0.4",
          "targets": [
            {
              "datasource": {
                "type": "prometheus",
                "uid": "000000003"
              },
              "exemplar": true,
              "expr": "sum(container_memory_rss{cluster=~\"$cluster\", namespace=\"$namespace\"})",
              "format": "time_series",
              "interval": "",
              "intervalFactor": 2,
              "legendFormat": "{{namespace}}",
              "refId": "A",
              "step": 10
            }
          ],
          "title": "Memory utilization (w/o cache)",
          "type": "stat"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "000000003"
          },
          "fieldConfig": {
            "defaults": {
              "color": {
                "mode": "thresholds"
              },
              "mappings": [],
              "thresholds": {
                "mode": "absolute",
                "steps": [
                  {
                    "color": "green"
                  },
                  {
                    "color": "red",
                    "value": 80
                  }
                ]
              },
              "unit": "Bps"
            },
            "overrides": []
          },
          "gridPos": {
            "h": 4,
            "w": 6,
            "x": 18,
            "y": 7
          },
          "id": 473,
          "interval": "10m",
          "options": {
            "colorMode": "value",
            "graphMode": "area",
            "justifyMode": "auto",
            "orientation": "auto",
            "reduceOptions": {
              "calcs": [
                "mean"
              ],
              "fields": "",
              "values": false
            },
            "textMode": "auto"
          },
          "pluginVersion": "9.0.4",
          "targets": [
            {
              "datasource": {
                "type": "prometheus",
                "uid": "000000003"
              },
              "exemplar": true,
              "expr": "sum(irate(container_network_receive_packets_total{cluster=~\"$cluster\", namespace=~\"$namespace\"}[$__rate_interval])) ",
              "interval": "",
              "legendFormat": "ingress",
              "refId": "A"
            },
            {
              "datasource": {
                "type": "prometheus",
                "uid": "000000003"
              },
              "exemplar": true,
              "expr": "sum(irate(container_network_transmit_packets_total{cluster=\"$cluster\", namespace=~\"$namespace\"}[$__rate_interval])) ",
              "hide": false,
              "interval": "",
              "legendFormat": "egress",
              "refId": "B"
            }
          ],
          "title": "Rate of Rx/Tx Packets",
          "type": "stat"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "000000003"
          },
          "fieldConfig": {
            "defaults": {
              "color": {
                "mode": "palette-classic"
              },
              "custom": {
                "axisLabel": "",
                "axisPlacement": "auto",
                "barAlignment": 0,
                "drawStyle": "line",
                "fillOpacity": 0,
                "gradientMode": "none",
                "hideFrom": {
                  "legend": false,
                  "tooltip": false,
                  "viz": false
                },
                "lineInterpolation": "linear",
                "lineStyle": {
                  "fill": "solid"
                },
                "lineWidth": 1,
                "pointSize": 5,
                "scaleDistribution": {
                  "type": "linear"
                },
                "showPoints": "auto",
                "spanNulls": true,
                "stacking": {
                  "group": "A",
                  "mode": "none"
                },
                "thresholdsStyle": {
                  "mode": "off"
                }
              },
              "mappings": [],
              "min": 0,
              "thresholds": {
                "mode": "absolute",
                "steps": [
                  {
                    "color": "green"
                  },
                  {
                    "color": "red",
                    "value": 80
                  }
                ]
              },
              "unit": "short"
            },
            "overrides": []
          },
          "gridPos": {
            "h": 6,
            "w": 12,
            "x": 0,
            "y": 11
          },
          "id": 330,
          "links": [],
          "options": {
            "legend": {
              "calcs": [
                "lastNotNull"
              ],
              "displayMode": "list",
              "placement": "bottom"
            },
            "tooltip": {
              "mode": "single",
              "sort": "none"
            }
          },
          "pluginVersion": "8.3.2",
          "targets": [
            {
              "datasource": {
                "type": "prometheus",
                "uid": "000000003"
              },
              "exemplar": true,
              "expr": "sum(node_namespace_pod_container:container_cpu_usage_seconds_total:sum_irate{cluster=~\"$cluster\",namespace=~\"$namespace\"})",
              "format": "time_series",
              "hide": true,
              "interval": "",
              "intervalFactor": 2,
              "legendFormat": "$namespace",
              "refId": "B",
              "step": 10
            },
            {
              "datasource": {
                "type": "prometheus",
                "uid": "000000003"
              },
              "exemplar": true,
              "expr": "sum(irate(container_cpu_usage_seconds_total{cluster=~\"$cluster\",namespace=~\"$namespace\"}[$__rate_interval]))",
              "format": "time_series",
              "hide": false,
              "interval": "",
              "intervalFactor": 2,
              "legendFormat": "$namespace",
              "refId": "C",
              "step": 10
            }
          ],
          "title": "Processor utilization by namespace",
          "type": "timeseries"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "000000003"
          },
          "fieldConfig": {
            "defaults": {
              "color": {
                "mode": "palette-classic"
              },
              "custom": {
                "axisLabel": "",
                "axisPlacement": "auto",
                "barAlignment": 0,
                "drawStyle": "line",
                "fillOpacity": 0,
                "gradientMode": "none",
                "hideFrom": {
                  "legend": false,
                  "tooltip": false,
                  "viz": false
                },
                "lineInterpolation": "linear",
                "lineWidth": 1,
                "pointSize": 5,
                "scaleDistribution": {
                  "type": "linear"
                },
                "showPoints": "auto",
                "spanNulls": false,
                "stacking": {
                  "group": "A",
                  "mode": "none"
                },
                "thresholdsStyle": {
                  "mode": "off"
                }
              },
              "mappings": [],
              "min": 0,
              "thresholds": {
                "mode": "absolute",
                "steps": [
                  {
                    "color": "green"
                  }
                ]
              },
              "unit": "bytes"
            },
            "overrides": []
          },
          "gridPos": {
            "h": 6,
            "w": 12,
            "x": 12,
            "y": 11
          },
          "id": 472,
          "links": [],
          "options": {
            "legend": {
              "calcs": [
                "lastNotNull"
              ],
              "displayMode": "list",
              "placement": "bottom"
            },
            "tooltip": {
              "mode": "single",
              "sort": "none"
            }
          },
          "pluginVersion": "8.3.2",
          "targets": [
            {
              "datasource": {
                "type": "prometheus",
                "uid": "000000003"
              },
              "exemplar": true,
              "expr": "sum(container_memory_rss{cluster=~\"$cluster\", container!=\"POD\", namespace=\"$namespace\"})",
              "format": "time_series",
              "interval": "",
              "intervalFactor": 2,
              "legendFormat": "$namespace",
              "refId": "A",
              "step": 10
            }
          ],
          "title": "Memory utilization (w/o cache) - Trend",
          "type": "timeseries"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "000000003"
          },
          "fieldConfig": {
            "defaults": {
              "color": {
                "mode": "thresholds"
              },
              "custom": {
                "align": "center",
                "displayMode": "auto",
                "inspect": false
              },
              "mappings": [],
              "noValue": "--",
              "thresholds": {
                "mode": "absolute",
                "steps": [
                  {
                    "color": "green"
                  },
                  {
                    "color": "red",
                    "value": 80
                  }
                ]
              },
              "unit": "none"
            },
            "overrides": [
              {
                "matcher": {
                  "id": "byName",
                  "options": "Used (%)"
                },
                "properties": [
                  {
                    "id": "decimals",
                    "value": 1
                  }
                ]
              },
              {
                "matcher": {
                  "id": "byName",
                  "options": "Status"
                },
                "properties": [
                  {
                    "id": "mappings",
                    "value": [
                      {
                        "options": {
                          "0": {
                            "text": "Bound"
                          },
                          "1": {
                            "text": "Pending"
                          },
                          "2": {
                            "text": "Lost"
                          }
                        },
                        "type": "value"
                      }
                    ]
                  },
                  {
                    "id": "noValue",
                    "value": "--"
                  },
                  {
                    "id": "custom.width",
                    "value": 118
                  }
                ]
              },
              {
                "matcher": {
                  "id": "byName",
                  "options": "StorageClass"
                },
                "properties": [
                  {
                    "id": "custom.width",
                    "value": 112
                  }
                ]
              },
              {
                "matcher": {
                  "id": "byName",
                  "options": "Capacity (GiB)"
                },
                "properties": [
                  {
                    "id": "custom.width",
                    "value": 109
                  }
                ]
              },
              {
                "matcher": {
                  "id": "byName",
                  "options": "Used (GiB)"
                },
                "properties": [
                  {
                    "id": "custom.width",
                    "value": 98
                  }
                ]
              },
              {
                "matcher": {
                  "id": "byName",
                  "options": "Available (GiB)"
                },
                "properties": [
                  {
                    "id": "custom.width",
                    "value": 116
                  }
                ]
              }
            ]
          },
          "gridPos": {
            "h": 7,
            "w": 24,
            "x": 0,
            "y": 17
          },
          "id": 455,
          "interval": "",
          "options": {
            "footer": {
              "fields": "",
              "reducer": [
                "sum"
              ],
              "show": false
            },
            "showHeader": true,
            "sortBy": []
          },
          "pluginVersion": "9.0.4",
          "targets": [
            {
              "datasource": {
                "type": "prometheus",
                "uid": "000000003"
              },
              "exemplar": false,
              "expr": " sum by (persistentvolumeclaim,namespace,storageclass,volumename)(kube_persistentvolumeclaim_info{namespace=~\"$namespace\",cluster=~\"$cluster\"})",
              "format": "table",
              "hide": false,
              "instant": true,
              "interval": "",
              "legendFormat": "",
              "refId": "A"
            },
            {
              "datasource": {
                "type": "prometheus",
                "uid": "000000003"
              },
              "exemplar": false,
              "expr": "sum by (persistentvolumeclaim,namespace) (kubelet_volume_stats_capacity_bytes{namespace=~\"$namespace\", cluster=~\"$cluster\"}/1024/1024/1024)",
              "format": "table",
              "hide": false,
              "instant": true,
              "interval": "",
              "legendFormat": "",
              "refId": "B"
            },
            {
              "datasource": {
                "type": "prometheus",
                "uid": "000000003"
              },
              "exemplar": false,
              "expr": "sum by (persistentvolumeclaim,namespace) (kubelet_volume_stats_used_bytes{namespace=~\"$namespace\", cluster=~\"$cluster\"}/1024/1024/1024)",
              "format": "table",
              "hide": false,
              "instant": true,
              "interval": "",
              "legendFormat": "",
              "refId": "C"
            },
            {
              "datasource": {
                "type": "prometheus",
                "uid": "000000003"
              },
              "exemplar": false,
              "expr": "sum by (persistentvolumeclaim,namespace) (kubelet_volume_stats_available_bytes{namespace=~\"$namespace\", cluster=~\"$cluster\"}/1024/1024/1024)",
              "format": "table",
              "hide": false,
              "instant": true,
              "interval": "",
              "legendFormat": "",
              "refId": "D"
            },
            {
              "datasource": {
                "type": "prometheus",
                "uid": "000000003"
              },
              "exemplar": false,
              "expr": "sum(kube_persistentvolumeclaim_status_phase{namespace=~\"$namespace\", cluster=~\"$cluster\",phase=~\"(Pending|Lost)\"}) by (persistentvolumeclaim,namespace) + sum(kube_persistentvolumeclaim_status_phase{namespace=~\"$namespace\", cluster=~\"$cluster\",phase=~\"(Lost)\"}) by (persistentvolumeclaim,namespace)",
              "format": "table",
              "hide": false,
              "instant": true,
              "interval": "",
              "legendFormat": "",
              "refId": "E"
            },
            {
              "datasource": {
                "type": "prometheus",
                "uid": "000000003"
              },
              "exemplar": false,
              "expr": "sum by (persistentvolumeclaim,namespace) (kubelet_volume_stats_used_bytes{namespace=~\"$namespace\", cluster=~\"$cluster\"}/kubelet_volume_stats_capacity_bytes{namespace=~\"$namespace\", cluster=~\"$cluster\"} * 100)",
              "format": "table",
              "hide": false,
              "instant": true,
              "interval": "",
              "legendFormat": "",
              "refId": "F"
            }
          ],
          "title": "Persistent Volume Claim",
          "transformations": [
            {
              "id": "merge",
              "options": {}
            },
            {
              "id": "organize",
              "options": {
                "excludeByName": {
                  "Time": true,
                  "Time 1": true,
                  "Time 2": true,
                  "Time 3": true,
                  "Time 4": true,
                  "Time 5": true,
                  "Time 6": true,
                  "Value #A": true
                },
                "indexByName": {},
                "renameByName": {
                  "Time 1": "",
                  "Time 2": "",
                  "Time 3": "",
                  "Time 4": "",
                  "Time 5": "",
                  "Time 6": "",
                  "Value #A": "",
                  "Value #B": "Capacity (GiB)",
                  "Value #C": "Used (GiB)",
                  "Value #D": "Available (GiB)",
                  "Value #E": "Status",
                  "Value #F": "Used (%)",
                  "namespace": "Namespace",
                  "persistentvolumeclaim": "PersistentVolumeClaim",
                  "storageclass": "StorageClass",
                  "volumename": "PhysicalVolume"
                }
              }
            }
          ],
          "type": "table"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "000000003"
          },
          "fieldConfig": {
            "defaults": {
              "color": {
                "mode": "palette-classic"
              },
              "custom": {
                "axisLabel": "",
                "axisPlacement": "auto",
                "axisSoftMin": 0,
                "barAlignment": 0,
                "drawStyle": "line",
                "fillOpacity": 4,
                "gradientMode": "none",
                "hideFrom": {
                  "legend": false,
                  "tooltip": false,
                  "viz": false
                },
                "lineInterpolation": "linear",
                "lineWidth": 1,
                "pointSize": 5,
                "scaleDistribution": {
                  "type": "linear"
                },
                "showPoints": "auto",
                "spanNulls": false,
                "stacking": {
                  "group": "A",
                  "mode": "none"
                },
                "thresholdsStyle": {
                  "mode": "off"
                }
              },
              "mappings": [],
              "thresholds": {
                "mode": "absolute",
                "steps": [
                  {
                    "color": "green"
                  },
                  {
                    "color": "red",
                    "value": 80
                  }
                ]
              },
              "unit": "Bps"
            },
            "overrides": []
          },
          "gridPos": {
            "h": 7,
            "w": 9,
            "x": 0,
            "y": 24
          },
          "id": 474,
          "interval": "10m",
          "options": {
            "legend": {
              "calcs": [],
              "displayMode": "list",
              "placement": "bottom"
            },
            "tooltip": {
              "mode": "single",
              "sort": "none"
            }
          },
          "targets": [
            {
              "datasource": {
                "type": "prometheus",
                "uid": "000000003"
              },
              "exemplar": true,
              "expr": "sum(irate(container_network_receive_packets_total{cluster=~\"$cluster\", namespace=~\"$namespace\"}[$__rate_interval])) ",
              "interval": "",
              "legendFormat": "$namespace: ingress",
              "refId": "A"
            },
            {
              "datasource": {
                "type": "prometheus",
                "uid": "000000003"
              },
              "exemplar": true,
              "expr": "sum(irate(container_network_transmit_packets_total{cluster=\"$cluster\", namespace=~\"$namespace\"}[$__rate_interval])) ",
              "hide": false,
              "interval": "",
              "legendFormat": "$namespace: egress",
              "refId": "B"
            }
          ],
          "title": "Network - Received vs Transmitted kB/s - Trend",
          "type": "timeseries"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "000000003"
          },
          "fieldConfig": {
            "defaults": {
              "color": {
                "mode": "thresholds"
              },
              "custom": {
                "align": "auto",
                "displayMode": "auto",
                "inspect": false
              },
              "decimals": 2,
              "displayName": "",
              "mappings": [],
              "thresholds": {
                "mode": "absolute",
                "steps": [
                  {
                    "color": "green"
                  },
                  {
                    "color": "red",
                    "value": 80
                  }
                ]
              },
              "unit": "short"
            },
            "overrides": [
              {
                "matcher": {
                  "id": "byName",
                  "options": "Time"
                },
                "properties": [
                  {
                    "id": "displayName",
                    "value": "Time"
                  },
                  {
                    "id": "custom.align"
                  }
                ]
              },
              {
                "matcher": {
                  "id": "byName",
                  "options": "Value #A"
                },
                "properties": [
                  {
                    "id": "displayName",
                    "value": "Receive Bandwidth"
                  },
                  {
                    "id": "unit",
                    "value": "Bps"
                  },
                  {
                    "id": "decimals",
                    "value": 2
                  },
                  {
                    "id": "custom.align",
                    "value": "center"
                  }
                ]
              },
              {
                "matcher": {
                  "id": "byName",
                  "options": "Value #B"
                },
                "properties": [
                  {
                    "id": "displayName",
                    "value": "Transmit andwidth"
                  },
                  {
                    "id": "unit",
                    "value": "Bps"
                  },
                  {
                    "id": "decimals",
                    "value": 2
                  },
                  {
                    "id": "custom.align",
                    "value": "center"
                  }
                ]
              },
              {
                "matcher": {
                  "id": "byName",
                  "options": "Value #C"
                },
                "properties": [
                  {
                    "id": "displayName",
                    "value": "Packets received rate"
                  },
                  {
                    "id": "unit",
                    "value": "pps"
                  },
                  {
                    "id": "decimals",
                    "value": 2
                  },
                  {
                    "id": "custom.align",
                    "value": "center"
                  }
                ]
              },
              {
                "matcher": {
                  "id": "byName",
                  "options": "Value #D"
                },
                "properties": [
                  {
                    "id": "displayName",
                    "value": "Packets transmitted rate"
                  },
                  {
                    "id": "unit",
                    "value": "pps"
                  },
                  {
                    "id": "decimals",
                    "value": 2
                  },
                  {
                    "id": "custom.align",
                    "value": "center"
                  }
                ]
              },
              {
                "matcher": {
                  "id": "byName",
                  "options": "Value #E"
                },
                "properties": [
                  {
                    "id": "displayName",
                    "value": "Rate of Received Packets Dropped"
                  },
                  {
                    "id": "unit",
                    "value": "pps"
                  },
                  {
                    "id": "decimals",
                    "value": 2
                  },
                  {
                    "id": "custom.align"
                  }
                ]
              },
              {
                "matcher": {
                  "id": "byName",
                  "options": "Value #F"
                },
                "properties": [
                  {
                    "id": "displayName",
                    "value": "Rate of Transmitted Packets Dropped"
                  },
                  {
                    "id": "unit",
                    "value": "pps"
                  },
                  {
                    "id": "decimals",
                    "value": 2
                  },
                  {
                    "id": "custom.align"
                  }
                ]
              },
              {
                "matcher": {
                  "id": "byName",
                  "options": "pod"
                },
                "properties": [
                  {
                    "id": "displayName",
                    "value": "Pod"
                  },
                  {
                    "id": "unit",
                    "value": "short"
                  },
                  {
                    "id": "decimals",
                    "value": 2
                  },
                  {
                    "id": "links",
                    "value": [
                      {
                        "targetBlank": false,
                        "title": "Drill down to pods",
                        "url": "./d/6581e46e4e5c7ba40a07646395ef7b23/k8s-resources-pod?var-datasource=$datasource&var-cluster=$cluster&var-namespace=$namespace&var-pod=$__cell"
                      }
                    ]
                  },
                  {
                    "id": "custom.align"
                  }
                ]
              },
              {
                "matcher": {
                  "id": "byName",
                  "options": "Receive Bandwidth"
                },
                "properties": [
                  {
                    "id": "custom.width",
                    "value": 140
                  }
                ]
              },
              {
                "matcher": {
                  "id": "byName",
                  "options": "Transmit andwidth"
                },
                "properties": [
                  {
                    "id": "custom.width",
                    "value": 135
                  }
                ]
              },
              {
                "matcher": {
                  "id": "byName",
                  "options": "Packets received rate"
                },
                "properties": [
                  {
                    "id": "custom.width",
                    "value": 154
                  }
                ]
              },
              {
                "matcher": {
                  "id": "byName",
                  "options": "Pod"
                },
                "properties": [
                  {
                    "id": "custom.width",
                    "value": 121
                  }
                ]
              }
            ]
          },
          "gridPos": {
            "h": 7,
            "w": 15,
            "x": 9,
            "y": 24
          },
          "id": 504,
          "interval": "1m",
          "links": [],
          "options": {
            "footer": {
              "fields": "",
              "reducer": [
                "sum"
              ],
              "show": false
            },
            "showHeader": true,
            "sortBy": []
          },
          "pluginVersion": "9.0.4",
          "targets": [
            {
              "datasource": {
                "type": "prometheus",
                "uid": "000000003"
              },
              "exemplar": false,
              "expr": "sum(irate(container_network_receive_bytes_total{cluster=\"$cluster\", namespace=~\"$namespace\"}[$__rate_interval])) by (pod)",
              "format": "table",
              "instant": true,
              "interval": "",
              "intervalFactor": 2,
              "legendFormat": "",
              "refId": "A",
              "step": 10
            },
            {
              "datasource": {
                "type": "prometheus",
                "uid": "000000003"
              },
              "exemplar": false,
              "expr": "sum(irate(container_network_transmit_bytes_total{cluster=\"$cluster\", namespace=~\"$namespace\"}[$__rate_interval])) by (pod)",
              "format": "table",
              "instant": true,
              "interval": "",
              "intervalFactor": 2,
              "legendFormat": "",
              "refId": "B",
              "step": 10
            },
            {
              "datasource": {
                "type": "prometheus",
                "uid": "000000003"
              },
              "exemplar": false,
              "expr": "sum(irate(container_network_receive_packets_total{cluster=\"$cluster\", namespace=~\"$namespace\"}[$__rate_interval])) by (pod)",
              "format": "table",
              "instant": true,
              "interval": "",
              "intervalFactor": 2,
              "legendFormat": "",
              "refId": "C",
              "step": 10
            },
            {
              "datasource": {
                "type": "prometheus",
                "uid": "000000003"
              },
              "exemplar": false,
              "expr": "sum(irate(container_network_transmit_packets_total{cluster=\"$cluster\", namespace=~\"$namespace\"}[$__rate_interval])) by (pod)",
              "format": "table",
              "instant": true,
              "interval": "",
              "intervalFactor": 2,
              "legendFormat": "",
              "refId": "D",
              "step": 10
            },
            {
              "datasource": {
                "type": "prometheus",
                "uid": "000000003"
              },
              "exemplar": false,
              "expr": "sum(irate(container_network_receive_packets_dropped_total{cluster=\"$cluster\", namespace=~\"$namespace\"}[$__rate_interval])) by (pod)",
              "format": "table",
              "hide": true,
              "instant": true,
              "interval": "",
              "intervalFactor": 2,
              "legendFormat": "",
              "refId": "E",
              "step": 10
            },
            {
              "datasource": {
                "type": "prometheus",
                "uid": "000000003"
              },
              "exemplar": false,
              "expr": "sum(irate(container_network_transmit_packets_dropped_total{cluster=\"$cluster\", namespace=~\"$namespace\"}[$__rate_interval])) by (pod)",
              "format": "table",
              "hide": true,
              "instant": true,
              "interval": "",
              "intervalFactor": 2,
              "legendFormat": "",
              "refId": "F",
              "step": 10
            }
          ],
          "title": "Current Network Usage",
          "transformations": [
            {
              "id": "merge",
              "options": {
                "reducers": []
              }
            },
            {
              "id": "organize",
              "options": {
                "excludeByName": {
                  "Time": true
                },
                "indexByName": {},
                "renameByName": {
                  "Value #A": "",
                  "Value #B": "",
                  "Value #C": "",
                  "Value #D": ""
                }
              }
            }
          ],
          "type": "table"
        }
      ],
      "targets": [
        {
          "datasource": {
            "type": "prometheus",
            "uid": "000000003"
          },
          "refId": "A"
        }
      ],
      "title": "Namespace ($namespace)",
      "type": "row"
    },
    {
      "collapsed": true,
      "datasource": {
        "type": "prometheus",
        "uid": "000000003"
      },
      "gridPos": {
        "h": 1,
        "w": 24,
        "x": 0,
        "y": 7
      },
      "id": 72,
      "panels": [
        {
          "datasource": {
            "type": "prometheus",
            "uid": "000000003"
          },
          "fieldConfig": {
            "defaults": {
              "color": {
                "mode": "thresholds"
              },
              "mappings": [],
              "thresholds": {
                "mode": "absolute",
                "steps": [
                  {
                    "color": "green"
                  },
                  {
                    "color": "red",
                    "value": 80
                  }
                ]
              }
            },
            "overrides": []
          },
          "gridPos": {
            "h": 4,
            "w": 3,
            "x": 0,
            "y": 8
          },
          "id": 74,
          "options": {
            "colorMode": "none",
            "graphMode": "none",
            "justifyMode": "center",
            "orientation": "auto",
            "reduceOptions": {
              "calcs": [
                "lastNotNull"
              ],
              "fields": "",
              "values": false
            },
            "textMode": "auto"
          },
          "pluginVersion": "9.0.4",
          "targets": [
            {
              "datasource": {
                "type": "prometheus",
                "uid": "000000003"
              },
              "exemplar": true,
              "expr": "sum(kube_pod_status_phase{namespace=~\"$namespace\",cluster=~\"$cluster\",job=~\"kube-state-metrics\", phase=\"Running\",pod=\"$pod\"})",
              "interval": "",
              "legendFormat": "",
              "refId": "A"
            }
          ],
          "title": "Pods Running",
          "type": "stat"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "000000003"
          },
          "fieldConfig": {
            "defaults": {
              "color": {
                "mode": "thresholds"
              },
              "mappings": [],
              "thresholds": {
                "mode": "absolute",
                "steps": [
                  {
                    "color": "green"
                  },
                  {
                    "color": "red",
                    "value": 80
                  }
                ]
              }
            },
            "overrides": []
          },
          "gridPos": {
            "h": 4,
            "w": 3,
            "x": 3,
            "y": 8
          },
          "id": 95,
          "options": {
            "colorMode": "none",
            "graphMode": "none",
            "justifyMode": "center",
            "orientation": "auto",
            "reduceOptions": {
              "calcs": [
                "lastNotNull"
              ],
              "fields": "",
              "values": false
            },
            "textMode": "auto"
          },
          "pluginVersion": "9.0.4",
          "targets": [
            {
              "datasource": {
                "type": "prometheus",
                "uid": "000000003"
              },
              "exemplar": true,
              "expr": " sum(kube_pod_status_phase{namespace=~\"$namespace\", cluster=~\"$cluster\", job=~\"kube-state-metrics\",phase=\"Failed\",pod=\"$pod\"})",
              "interval": "",
              "legendFormat": "",
              "refId": "A"
            }
          ],
          "title": "Pods Failed",
          "type": "stat"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "000000003"
          },
          "fieldConfig": {
            "defaults": {
              "color": {
                "mode": "thresholds"
              },
              "mappings": [],
              "thresholds": {
                "mode": "absolute",
                "steps": [
                  {
                    "color": "green"
                  },
                  {
                    "color": "red",
                    "value": 80
                  }
                ]
              }
            },
            "overrides": []
          },
          "gridPos": {
            "h": 4,
            "w": 3,
            "x": 6,
            "y": 8
          },
          "id": 114,
          "options": {
            "colorMode": "none",
            "graphMode": "none",
            "justifyMode": "center",
            "orientation": "auto",
            "reduceOptions": {
              "calcs": [
                "lastNotNull"
              ],
              "fields": "",
              "values": false
            },
            "textMode": "auto"
          },
          "pluginVersion": "9.0.4",
          "targets": [
            {
              "datasource": {
                "type": "prometheus",
                "uid": "000000003"
              },
              "exemplar": true,
              "expr": " sum(kube_pod_status_phase{namespace=~\"$namespace\", cluster=~\"$cluster\",job=~\"kube-state-metrics\",phase=\"Pending\",pod=\"$pod\"})",
              "interval": "",
              "legendFormat": "",
              "refId": "A"
            }
          ],
          "title": "Pods Pending",
          "type": "stat"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "000000003"
          },
          "fieldConfig": {
            "defaults": {
              "color": {
                "mode": "thresholds"
              },
              "mappings": [],
              "thresholds": {
                "mode": "absolute",
                "steps": [
                  {
                    "color": "green"
                  },
                  {
                    "color": "red",
                    "value": 80
                  }
                ]
              }
            },
            "overrides": []
          },
          "gridPos": {
            "h": 4,
            "w": 3,
            "x": 9,
            "y": 8
          },
          "id": 201,
          "options": {
            "colorMode": "none",
            "graphMode": "none",
            "justifyMode": "center",
            "orientation": "auto",
            "reduceOptions": {
              "calcs": [
                "lastNotNull"
              ],
              "fields": "",
              "values": false
            },
            "textMode": "auto"
          },
          "pluginVersion": "9.0.4",
          "targets": [
            {
              "datasource": {
                "type": "prometheus",
                "uid": "000000003"
              },
              "exemplar": true,
              "expr": " sum(kube_pod_status_phase{namespace=~\"$namespace\", cluster=~\"$cluster\",phase=\"Succeeded\",job=~\"kube-state-metrics\",pod=\"$pod\"})",
              "interval": "",
              "legendFormat": "",
              "refId": "A"
            }
          ],
          "title": "Pods Succeeded",
          "type": "stat"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "000000003"
          },
          "fieldConfig": {
            "defaults": {
              "color": {
                "mode": "thresholds"
              },
              "mappings": [],
              "thresholds": {
                "mode": "absolute",
                "steps": [
                  {
                    "color": "green"
                  },
                  {
                    "color": "red",
                    "value": 80
                  }
                ]
              }
            },
            "overrides": []
          },
          "gridPos": {
            "h": 4,
            "w": 3,
            "x": 12,
            "y": 8
          },
          "id": 202,
          "options": {
            "colorMode": "none",
            "graphMode": "none",
            "justifyMode": "center",
            "orientation": "auto",
            "reduceOptions": {
              "calcs": [
                "lastNotNull"
              ],
              "fields": "",
              "values": false
            },
            "textMode": "auto"
          },
          "pluginVersion": "9.0.4",
          "targets": [
            {
              "datasource": {
                "type": "prometheus",
                "uid": "000000003"
              },
              "exemplar": true,
              "expr": " sum(kube_pod_status_phase{namespace=~\"$namespace\", cluster=~\"$cluster\",phase=\"Unknown\"})",
              "interval": "",
              "legendFormat": "",
              "refId": "A"
            }
          ],
          "title": "Pods Unknown",
          "type": "stat"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "000000003"
          },
          "fieldConfig": {
            "defaults": {
              "color": {
                "mode": "thresholds"
              },
              "mappings": [],
              "min": 0,
              "thresholds": {
                "mode": "absolute",
                "steps": [
                  {
                    "color": "green"
                  }
                ]
              },
              "unit": "decbytes"
            },
            "overrides": []
          },
          "gridPos": {
            "h": 4,
            "w": 3,
            "x": 15,
            "y": 8
          },
          "id": 506,
          "links": [],
          "options": {
            "colorMode": "value",
            "graphMode": "area",
            "justifyMode": "auto",
            "orientation": "auto",
            "reduceOptions": {
              "calcs": [
                "lastNotNull"
              ],
              "fields": "",
              "values": false
            },
            "textMode": "auto"
          },
          "pluginVersion": "9.0.4",
          "targets": [
            {
              "datasource": {
                "type": "prometheus",
                "uid": "000000003"
              },
              "exemplar": true,
              "expr": "sum(container_memory_rss{cluster=~\"$cluster\", namespace=~\"$namespace\",pod=~\"$pod\"})",
              "format": "time_series",
              "interval": "",
              "intervalFactor": 2,
              "legendFormat": "{{pod}}",
              "refId": "A",
              "step": 10
            }
          ],
          "title": "Memory utilization (w/o cache)",
          "type": "stat"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "000000003"
          },
          "fieldConfig": {
            "defaults": {
              "color": {
                "mode": "thresholds"
              },
              "mappings": [],
              "thresholds": {
                "mode": "absolute",
                "steps": [
                  {
                    "color": "green"
                  },
                  {
                    "color": "red",
                    "value": 80
                  }
                ]
              },
              "unit": "Bps"
            },
            "overrides": []
          },
          "gridPos": {
            "h": 4,
            "w": 6,
            "x": 18,
            "y": 8
          },
          "id": 507,
          "interval": "10m",
          "options": {
            "colorMode": "value",
            "graphMode": "area",
            "justifyMode": "auto",
            "orientation": "auto",
            "reduceOptions": {
              "calcs": [
                "mean"
              ],
              "fields": "",
              "values": false
            },
            "textMode": "auto"
          },
          "pluginVersion": "9.0.4",
          "targets": [
            {
              "datasource": {
                "type": "prometheus",
                "uid": "000000003"
              },
              "exemplar": true,
              "expr": "sum(irate(container_network_receive_packets_total{cluster=~\"$cluster\", namespace=~\"$namespace\",pod=~\"$pod\"}[$__rate_interval])) ",
              "interval": "",
              "legendFormat": "ingress",
              "refId": "A"
            },
            {
              "datasource": {
                "type": "prometheus",
                "uid": "000000003"
              },
              "exemplar": true,
              "expr": "sum(irate(container_network_transmit_packets_total{cluster=\"$cluster\", namespace=~\"$namespace\",pod=~\"$pod\"}[$__rate_interval])) ",
              "hide": false,
              "interval": "",
              "legendFormat": "egress",
              "refId": "B"
            }
          ],
          "title": "Rate of Rx/Tx Packets",
          "type": "stat"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "000000003"
          },
          "fieldConfig": {
            "defaults": {
              "color": {
                "mode": "palette-classic"
              },
              "custom": {
                "axisLabel": "",
                "axisPlacement": "auto",
                "barAlignment": 0,
                "drawStyle": "line",
                "fillOpacity": 0,
                "gradientMode": "none",
                "hideFrom": {
                  "legend": false,
                  "tooltip": false,
                  "viz": false
                },
                "lineInterpolation": "linear",
                "lineWidth": 1,
                "pointSize": 5,
                "scaleDistribution": {
                  "type": "linear"
                },
                "showPoints": "auto",
                "spanNulls": true,
                "stacking": {
                  "group": "A",
                  "mode": "none"
                },
                "thresholdsStyle": {
                  "mode": "off"
                }
              },
              "mappings": [],
              "min": 0,
              "thresholds": {
                "mode": "absolute",
                "steps": [
                  {
                    "color": "green"
                  },
                  {
                    "color": "red",
                    "value": 80
                  }
                ]
              },
              "unit": "short"
            },
            "overrides": [
              {
                "matcher": {
                  "id": "byName",
                  "options": "quota - requests"
                },
                "properties": [
                  {
                    "id": "color",
                    "value": {
                      "fixedColor": "#F2495C",
                      "mode": "fixed"
                    }
                  },
                  {
                    "id": "custom.fillOpacity",
                    "value": 0
                  },
                  {
                    "id": "custom.lineWidth",
                    "value": 2
                  },
                  {
                    "id": "custom.stacking",
                    "value": {
                      "group": false,
                      "mode": "normal"
                    }
                  },
                  {
                    "id": "custom.lineStyle",
                    "value": {
                      "dash": [
                        10,
                        10
                      ],
                      "fill": "dash"
                    }
                  }
                ]
              },
              {
                "matcher": {
                  "id": "byName",
                  "options": "quota - limits"
                },
                "properties": [
                  {
                    "id": "color",
                    "value": {
                      "fixedColor": "#FF9830",
                      "mode": "fixed"
                    }
                  },
                  {
                    "id": "custom.fillOpacity",
                    "value": 0
                  },
                  {
                    "id": "custom.lineWidth",
                    "value": 2
                  },
                  {
                    "id": "custom.stacking",
                    "value": {
                      "group": false,
                      "mode": "normal"
                    }
                  },
                  {
                    "id": "custom.lineStyle",
                    "value": {
                      "dash": [
                        10,
                        10
                      ],
                      "fill": "dash"
                    }
                  }
                ]
              }
            ]
          },
          "gridPos": {
            "h": 7,
            "w": 12,
            "x": 0,
            "y": 12
          },
          "id": 502,
          "links": [],
          "options": {
            "legend": {
              "calcs": [
                "lastNotNull"
              ],
              "displayMode": "list",
              "placement": "bottom"
            },
            "tooltip": {
              "mode": "single",
              "sort": "none"
            }
          },
          "pluginVersion": "8.3.2",
          "targets": [
            {
              "datasource": {
                "type": "prometheus",
                "uid": "000000003"
              },
              "exemplar": true,
              "expr": "sum(irate(container_cpu_usage_seconds_total{cluster=\"$cluster\", namespace=\"$namespace\",pod=\"$pod\"}[$__rate_interval]))",
              "format": "time_series",
              "hide": false,
              "interval": "",
              "intervalFactor": 1,
              "legendFormat": "$pod",
              "refId": "A",
              "step": 10
            },
            {
              "datasource": {
                "type": "prometheus",
                "uid": "000000003"
              },
              "expr": "scalar(kube_resourcequota{cluster=\"$cluster\", namespace=\"$namespace\", type=\"hard\",resource=\"requests.cpu\"})",
              "format": "time_series",
              "hide": true,
              "intervalFactor": 2,
              "legendFormat": "quota - requests",
              "refId": "B",
              "step": 10
            },
            {
              "datasource": {
                "type": "prometheus",
                "uid": "000000003"
              },
              "exemplar": true,
              "expr": "scalar(kube_resourcequota{cluster=\"$cluster\", namespace=\"$namespace\", type=\"hard\",resource=\"limits.cpu\"})",
              "format": "time_series",
              "hide": true,
              "interval": "",
              "intervalFactor": 2,
              "legendFormat": "quota - limits",
              "refId": "C",
              "step": 10
            },
            {
              "datasource": {
                "type": "prometheus",
                "uid": "000000003"
              },
              "exemplar": true,
              "expr": "sum(node_namespace_pod_container:container_cpu_usage_seconds_total:sum_irate{cluster=\"$cluster\", namespace=\"$namespace\",pod=\"$pod\"})",
              "format": "time_series",
              "hide": true,
              "interval": "",
              "intervalFactor": 1,
              "legendFormat": "$pod",
              "refId": "D",
              "step": 10
            }
          ],
          "title": "Processor Utilization by Pod",
          "type": "timeseries"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "000000003"
          },
          "description": "Pods memory used ",
          "fieldConfig": {
            "defaults": {
              "color": {
                "mode": "palette-classic"
              },
              "custom": {
                "axisLabel": "",
                "axisPlacement": "auto",
                "barAlignment": 0,
                "drawStyle": "line",
                "fillOpacity": 44,
                "gradientMode": "opacity",
                "hideFrom": {
                  "legend": false,
                  "tooltip": false,
                  "viz": false
                },
                "lineInterpolation": "linear",
                "lineWidth": 1,
                "pointSize": 5,
                "scaleDistribution": {
                  "type": "linear"
                },
                "showPoints": "never",
                "spanNulls": true,
                "stacking": {
                  "group": "A",
                  "mode": "none"
                },
                "thresholdsStyle": {
                  "mode": "off"
                }
              },
              "mappings": [],
              "thresholds": {
                "mode": "absolute",
                "steps": [
                  {
                    "color": "green"
                  },
                  {
                    "color": "red",
                    "value": 80
                  }
                ]
              },
              "unit": "decbytes"
            },
            "overrides": []
          },
          "gridPos": {
            "h": 7,
            "w": 12,
            "x": 12,
            "y": 12
          },
          "id": 152,
          "options": {
            "legend": {
              "calcs": [
                "lastNotNull"
              ],
              "displayMode": "list",
              "placement": "bottom"
            },
            "tooltip": {
              "mode": "single",
              "sort": "none"
            }
          },
          "targets": [
            {
              "datasource": {
                "type": "prometheus",
                "uid": "000000003"
              },
              "exemplar": true,
              "expr": "sum(container_memory_working_set_bytes{cluster=\"$cluster\", namespace=~\"$namespace\", container!=\"\", image!=\"\",pod=~\"$pod\"}) by (pod)",
              "hide": false,
              "interval": "",
              "legendFormat": "{{pod}}",
              "refId": "A"
            }
          ],
          "title": " Memory usage  by Pod -- Trend",
          "type": "timeseries"
        }
      ],
      "targets": [
        {
          "datasource": {
            "type": "prometheus",
            "uid": "000000003"
          },
          "refId": "A"
        }
      ],
      "title": "Pod ($pod)",
      "type": "row"
    },
    {
      "collapsed": true,
      "datasource": {
        "type": "prometheus",
        "uid": "000000003"
      },
      "gridPos": {
        "h": 1,
        "w": 24,
        "x": 0,
        "y": 8
      },
      "id": 104,
      "panels": [
        {
          "datasource": {
            "type": "prometheus",
            "uid": "000000003"
          },
          "fieldConfig": {
            "defaults": {
              "color": {
                "mode": "thresholds"
              },
              "mappings": [],
              "thresholds": {
                "mode": "absolute",
                "steps": [
                  {
                    "color": "green"
                  },
                  {
                    "color": "red",
                    "value": 80
                  }
                ]
              }
            },
            "overrides": []
          },
          "gridPos": {
            "h": 5,
            "w": 3,
            "x": 0,
            "y": 17
          },
          "id": 108,
          "options": {
            "colorMode": "none",
            "graphMode": "none",
            "justifyMode": "auto",
            "orientation": "horizontal",
            "reduceOptions": {
              "calcs": [
                "lastNotNull"
              ],
              "fields": "",
              "values": false
            },
            "textMode": "auto"
          },
          "pluginVersion": "9.0.4",
          "targets": [
            {
              "datasource": {
                "type": "prometheus",
                "uid": "000000003"
              },
              "exemplar": true,
              "expr": "sum(kube_pod_container_status_running{namespace=~\"$namespace\",cluster=~\"$cluster\",pod=\"$pod\",job=~\"kube-state-metrics\",container!=\"POD\"})",
              "interval": "",
              "legendFormat": "",
              "refId": "A"
            }
          ],
          "title": "Containers Running",
          "type": "stat"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "000000003"
          },
          "fieldConfig": {
            "defaults": {
              "color": {
                "mode": "thresholds"
              },
              "mappings": [],
              "thresholds": {
                "mode": "absolute",
                "steps": [
                  {
                    "color": "green"
                  },
                  {
                    "color": "red",
                    "value": 80
                  }
                ]
              }
            },
            "overrides": []
          },
          "gridPos": {
            "h": 5,
            "w": 3,
            "x": 3,
            "y": 17
          },
          "id": 110,
          "options": {
            "colorMode": "none",
            "graphMode": "none",
            "justifyMode": "auto",
            "orientation": "horizontal",
            "reduceOptions": {
              "calcs": [
                "lastNotNull"
              ],
              "fields": "",
              "values": false
            },
            "textMode": "auto"
          },
          "pluginVersion": "9.0.4",
          "targets": [
            {
              "datasource": {
                "type": "prometheus",
                "uid": "000000003"
              },
              "exemplar": true,
              "expr": "sum(kube_pod_container_status_terminated{namespace=~\"$namespace\",cluster=~\"$cluster\",pod=\"$pod\",job=~\"kube-state-metrics\",container!=\"POD\"})",
              "interval": "",
              "legendFormat": "",
              "refId": "A"
            }
          ],
          "title": "Containers Terminated",
          "type": "stat"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "000000003"
          },
          "fieldConfig": {
            "defaults": {
              "color": {
                "mode": "thresholds"
              },
              "mappings": [],
              "thresholds": {
                "mode": "absolute",
                "steps": [
                  {
                    "color": "green"
                  },
                  {
                    "color": "red",
                    "value": 80
                  }
                ]
              }
            },
            "overrides": []
          },
          "gridPos": {
            "h": 5,
            "w": 3,
            "x": 6,
            "y": 17
          },
          "id": 112,
          "options": {
            "colorMode": "none",
            "graphMode": "none",
            "justifyMode": "auto",
            "orientation": "horizontal",
            "reduceOptions": {
              "calcs": [
                "lastNotNull"
              ],
              "fields": "",
              "values": false
            },
            "textMode": "auto"
          },
          "pluginVersion": "9.0.4",
          "targets": [
            {
              "datasource": {
                "type": "prometheus",
                "uid": "000000003"
              },
              "exemplar": true,
              "expr": "sum(kube_pod_container_status_waiting{namespace=~\"$namespace\",cluster=~\"$cluster\",pod=\"$pod\",job=~\"kube-state-metrics\",container!=\"POD\"})",
              "interval": "",
              "legendFormat": "",
              "refId": "A"
            }
          ],
          "title": "Containers waiting",
          "type": "stat"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "000000003"
          },
          "fieldConfig": {
            "defaults": {
              "color": {
                "mode": "thresholds"
              },
              "mappings": [],
              "thresholds": {
                "mode": "absolute",
                "steps": [
                  {
                    "color": "green"
                  },
                  {
                    "color": "red",
                    "value": 80
                  }
                ]
              }
            },
            "overrides": []
          },
          "gridPos": {
            "h": 5,
            "w": 4,
            "x": 9,
            "y": 17
          },
          "id": 324,
          "options": {
            "colorMode": "none",
            "graphMode": "none",
            "justifyMode": "center",
            "orientation": "auto",
            "reduceOptions": {
              "calcs": [
                "lastNotNull"
              ],
              "fields": "",
              "values": false
            },
            "textMode": "auto"
          },
          "pluginVersion": "9.0.4",
          "targets": [
            {
              "datasource": {
                "type": "prometheus",
                "uid": "000000003"
              },
              "exemplar": true,
              "expr": "sum(delta(kube_pod_container_status_restarts_total{namespace=~\"$namespace\",cluster=~\"$cluster\",pod=\"$pod\",job=~\"kube-state-metrics\",container!=\"POD\"}[30m]))",
              "interval": "",
              "legendFormat": "",
              "refId": "A"
            }
          ],
          "title": "Containers Restarts (Last 30 Minutes)",
          "type": "stat"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "000000003"
          },
          "fieldConfig": {
            "defaults": {
              "color": {
                "mode": "palette-classic"
              },
              "custom": {
                "axisLabel": "",
                "axisPlacement": "auto",
                "barAlignment": 0,
                "drawStyle": "line",
                "fillOpacity": 3,
                "gradientMode": "none",
                "hideFrom": {
                  "legend": false,
                  "tooltip": false,
                  "viz": false
                },
                "lineInterpolation": "linear",
                "lineStyle": {
                  "fill": "solid"
                },
                "lineWidth": 2,
                "pointSize": 4,
                "scaleDistribution": {
                  "type": "linear"
                },
                "showPoints": "auto",
                "spanNulls": true,
                "stacking": {
                  "group": "A",
                  "mode": "none"
                },
                "thresholdsStyle": {
                  "mode": "off"
                }
              },
              "mappings": [],
              "thresholds": {
                "mode": "absolute",
                "steps": [
                  {
                    "color": "green"
                  },
                  {
                    "color": "red",
                    "value": 80
                  }
                ]
              }
            },
            "overrides": []
          },
          "gridPos": {
            "h": 14,
            "w": 11,
            "x": 13,
            "y": 17
          },
          "id": 521,
          "options": {
            "legend": {
              "calcs": [
                "lastNotNull"
              ],
              "displayMode": "list",
              "placement": "bottom"
            },
            "tooltip": {
              "mode": "single",
              "sort": "none"
            }
          },
          "targets": [
            {
              "datasource": {
                "type": "prometheus",
                "uid": "000000003"
              },
              "editorMode": "code",
              "expr": "sum(irate(container_cpu_usage_seconds_total{cluster=\"$cluster\",namespace=\"$namespace\",pod=\"$pod\",container!=\"POD\"}[$__rate_interval])) by (container)",
              "legendFormat": "{{container}}",
              "range": true,
              "refId": "A"
            }
          ],
          "title": "Processor utilization by container",
          "type": "timeseries"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "000000003"
          },
          "fieldConfig": {
            "defaults": {
              "color": {
                "mode": "palette-classic"
              },
              "custom": {
                "axisLabel": "",
                "axisPlacement": "auto",
                "barAlignment": 0,
                "drawStyle": "line",
                "fillOpacity": 0,
                "gradientMode": "none",
                "hideFrom": {
                  "legend": false,
                  "tooltip": false,
                  "viz": false
                },
                "lineInterpolation": "linear",
                "lineWidth": 1,
                "pointSize": 5,
                "scaleDistribution": {
                  "type": "linear"
                },
                "showPoints": "auto",
                "spanNulls": true,
                "stacking": {
                  "group": "A",
                  "mode": "none"
                },
                "thresholdsStyle": {
                  "mode": "off"
                }
              },
              "mappings": [],
              "thresholds": {
                "mode": "absolute",
                "steps": [
                  {
                    "color": "green"
                  },
                  {
                    "color": "red",
                    "value": 80
                  }
                ]
              },
              "unit": "decbytes"
            },
            "overrides": []
          },
          "gridPos": {
            "h": 9,
            "w": 13,
            "x": 0,
            "y": 22
          },
          "id": 519,
          "options": {
            "legend": {
              "calcs": [
                "lastNotNull"
              ],
              "displayMode": "list",
              "placement": "bottom"
            },
            "tooltip": {
              "mode": "single",
              "sort": "none"
            }
          },
          "targets": [
            {
              "datasource": {
                "type": "prometheus",
                "uid": "000000003"
              },
              "editorMode": "code",
              "exemplar": false,
              "expr": "sum(container_memory_working_set_bytes{cluster=\"$cluster\", namespace=~\"$namespace\", container!=\"POD\", image!=\"\",pod=~\"$pod\"}) by (container)",
              "format": "time_series",
              "instant": false,
              "legendFormat": "{{container}}",
              "range": true,
              "refId": "A"
            }
          ],
          "title": " Memory usage  by container -- Trend",
          "type": "timeseries"
        }
      ],
      "targets": [
        {
          "datasource": {
            "type": "prometheus",
            "uid": "000000003"
          },
          "refId": "A"
        }
      ],
      "title": "Container ($pod)",
      "type": "row"
    },
    {
      "collapsed": true,
      "gridPos": {
        "h": 1,
        "w": 24,
        "x": 0,
        "y": 9
      },
      "id": 544,
      "panels": [
        {
          "datasource": {
            "type": "prometheus",
            "uid": "000000003"
          },
          "fieldConfig": {
            "defaults": {
              "color": {
                "mode": "palette-classic"
              },
              "custom": {
                "axisLabel": "",
                "axisPlacement": "auto",
                "barAlignment": 0,
                "drawStyle": "line",
                "fillOpacity": 0,
                "gradientMode": "none",
                "hideFrom": {
                  "legend": false,
                  "tooltip": false,
                  "viz": false
                },
                "lineInterpolation": "linear",
                "lineWidth": 1,
                "pointSize": 5,
                "scaleDistribution": {
                  "type": "linear"
                },
                "showPoints": "auto",
                "spanNulls": false,
                "stacking": {
                  "group": "A",
                  "mode": "none"
                },
                "thresholdsStyle": {
                  "mode": "off"
                }
              },
              "mappings": [],
              "thresholds": {
                "mode": "absolute",
                "steps": [
                  {
                    "color": "green"
                  },
                  {
                    "color": "red",
                    "value": 80
                  }
                ]
              }
            },
            "overrides": []
          },
          "gridPos": {
            "h": 8,
            "w": 12,
            "x": 0,
            "y": 10
          },
          "id": 540,
          "options": {
            "legend": {
              "calcs": [],
              "displayMode": "list",
              "placement": "bottom"
            },
            "tooltip": {
              "mode": "single",
              "sort": "none"
            }
          },
          "targets": [
            {
              "datasource": {
                "type": "prometheus",
                "uid": "000000003"
              },
              "expr": "max_over_time(prometheus_tsdb_head_series{cluster=~\"$cluster\"}[1d])",
              "refId": "A"
            }
          ],
          "title": "Prometheus TSDB",
          "type": "timeseries"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "000000003"
          },
          "fieldConfig": {
            "defaults": {
              "color": {
                "mode": "palette-classic"
              },
              "custom": {
                "axisLabel": "",
                "axisPlacement": "auto",
                "barAlignment": 0,
                "drawStyle": "line",
                "fillOpacity": 0,
                "gradientMode": "none",
                "hideFrom": {
                  "legend": false,
                  "tooltip": false,
                  "viz": false
                },
                "lineInterpolation": "linear",
                "lineWidth": 1,
                "pointSize": 5,
                "scaleDistribution": {
                  "type": "linear"
                },
                "showPoints": "auto",
                "spanNulls": false,
                "stacking": {
                  "group": "A",
                  "mode": "none"
                },
                "thresholdsStyle": {
                  "mode": "off"
                }
              },
              "mappings": [],
              "thresholds": {
                "mode": "absolute",
                "steps": [
                  {
                    "color": "green"
                  },
                  {
                    "color": "red",
                    "value": 80
                  }
                ]
              }
            },
            "overrides": []
          },
          "gridPos": {
            "h": 8,
            "w": 12,
            "x": 12,
            "y": 10
          },
          "id": 552,
          "options": {
            "legend": {
              "calcs": [],
              "displayMode": "list",
              "placement": "bottom"
            },
            "tooltip": {
              "mode": "single",
              "sort": "none"
            }
          },
          "targets": [
            {
              "datasource": {
                "type": "prometheus",
                "uid": "000000003"
              },
              "expr": "rate(prometheus_tsdb_head_series_created_total{cluster=~\"$cluster\"}[5m])",
              "refId": "A"
            }
          ],
          "title": "Time Series Created",
          "type": "timeseries"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "000000003"
          },
          "fieldConfig": {
            "defaults": {
              "color": {
                "mode": "palette-classic"
              },
              "custom": {
                "axisLabel": "",
                "axisPlacement": "auto",
                "barAlignment": 0,
                "drawStyle": "line",
                "fillOpacity": 0,
                "gradientMode": "none",
                "hideFrom": {
                  "legend": false,
                  "tooltip": false,
                  "viz": false
                },
                "lineInterpolation": "linear",
                "lineWidth": 1,
                "pointSize": 5,
                "scaleDistribution": {
                  "type": "linear"
                },
                "showPoints": "auto",
                "spanNulls": false,
                "stacking": {
                  "group": "A",
                  "mode": "none"
                },
                "thresholdsStyle": {
                  "mode": "off"
                }
              },
              "mappings": [],
              "thresholds": {
                "mode": "absolute",
                "steps": [
                  {
                    "color": "green"
                  },
                  {
                    "color": "red",
                    "value": 80
                  }
                ]
              }
            },
            "overrides": []
          },
          "gridPos": {
            "h": 8,
            "w": 12,
            "x": 0,
            "y": 18
          },
          "id": 548,
          "options": {
            "legend": {
              "calcs": [],
              "displayMode": "list",
              "placement": "bottom"
            },
            "tooltip": {
              "mode": "single",
              "sort": "none"
            }
          },
          "targets": [
            {
              "datasource": {
                "type": "prometheus",
                "uid": "000000003"
              },
              "expr": "rate(prometheus_tsdb_head_samples_appended_total{cluster=~\"$cluster\"}[5m])",
              "refId": "A"
            }
          ],
          "title": "Samples ingested",
          "type": "timeseries"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "000000003"
          },
          "fieldConfig": {
            "defaults": {
              "color": {
                "mode": "palette-classic"
              },
              "custom": {
                "axisLabel": "",
                "axisPlacement": "auto",
                "barAlignment": 0,
                "drawStyle": "line",
                "fillOpacity": 0,
                "gradientMode": "none",
                "hideFrom": {
                  "legend": false,
                  "tooltip": false,
                  "viz": false
                },
                "lineInterpolation": "linear",
                "lineWidth": 1,
                "pointSize": 5,
                "scaleDistribution": {
                  "type": "linear"
                },
                "showPoints": "auto",
                "spanNulls": false,
                "stacking": {
                  "group": "A",
                  "mode": "none"
                },
                "thresholdsStyle": {
                  "mode": "off"
                }
              },
              "mappings": [],
              "thresholds": {
                "mode": "absolute",
                "steps": [
                  {
                    "color": "green"
                  },
                  {
                    "color": "red",
                    "value": 80
                  }
                ]
              }
            },
            "overrides": []
          },
          "gridPos": {
            "h": 8,
            "w": 12,
            "x": 12,
            "y": 18
          },
          "id": 546,
          "options": {
            "legend": {
              "calcs": [],
              "displayMode": "list",
              "placement": "bottom"
            },
            "tooltip": {
              "mode": "single",
              "sort": "none"
            }
          },
          "targets": [
            {
              "datasource": {
                "type": "prometheus",
                "uid": "000000003"
              },
              "expr": "rate(prometheus_tsdb_head_series_removed_total{cluster=~\"$cluster\"}[5m])",
              "refId": "A"
            }
          ],
          "title": "Time Series Deleted ",
          "type": "timeseries"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "000000003"
          },
          "fieldConfig": {
            "defaults": {
              "color": {
                "mode": "palette-classic"
              },
              "custom": {
                "axisLabel": "",
                "axisPlacement": "auto",
                "barAlignment": 0,
                "drawStyle": "line",
                "fillOpacity": 0,
                "gradientMode": "none",
                "hideFrom": {
                  "legend": false,
                  "tooltip": false,
                  "viz": false
                },
                "lineInterpolation": "linear",
                "lineWidth": 1,
                "pointSize": 5,
                "scaleDistribution": {
                  "type": "linear"
                },
                "showPoints": "auto",
                "spanNulls": false,
                "stacking": {
                  "group": "A",
                  "mode": "none"
                },
                "thresholdsStyle": {
                  "mode": "off"
                }
              },
              "mappings": [],
              "thresholds": {
                "mode": "absolute",
                "steps": [
                  {
                    "color": "green"
                  },
                  {
                    "color": "red",
                    "value": 80
                  }
                ]
              }
            },
            "overrides": []
          },
          "gridPos": {
            "h": 8,
            "w": 12,
            "x": 0,
            "y": 26
          },
          "id": 550,
          "options": {
            "legend": {
              "calcs": [],
              "displayMode": "list",
              "placement": "bottom"
            },
            "tooltip": {
              "mode": "single",
              "sort": "none"
            }
          },
          "targets": [
            {
              "datasource": {
                "type": "prometheus",
                "uid": "000000003"
              },
              "expr": "sum by (job)(scrape_samples_scraped{cluster=~\"$cluster\"})",
              "refId": "A"
            }
          ],
          "title": "Samples scraped per job ",
          "type": "timeseries"
        }
      ],
      "title": "prometheus ",
      "type": "row"
    },
    {
      "collapsed": false,
      "gridPos": {
        "h": 1,
        "w": 24,
        "x": 0,
        "y": 10
      },
      "id": 556,
      "panels": [],
      "title": "Replicas",
      "type": "row"
    },
    {
      "datasource": {
        "type": "prometheus",
        "uid": "000000003"
      },
      "fieldConfig": {
        "defaults": {
          "color": {
            "mode": "thresholds"
          },
          "custom": {
            "align": "auto",
            "displayMode": "color-text",
            "inspect": false
          },
          "mappings": [],
          "thresholds": {
            "mode": "absolute",
            "steps": [
              {
                "color": "green",
                "value": null
              },
              {
                "color": "red",
                "value": 80
              }
            ]
          }
        },
        "overrides": [
          {
            "matcher": {
              "id": "byName",
              "options": "Time"
            },
            "properties": [
              {
                "id": "custom.width",
                "value": 211
              }
            ]
          },
          {
            "matcher": {
              "id": "byName",
              "options": "cluster"
            },
            "properties": [
              {
                "id": "custom.width",
                "value": 275
              }
            ]
          },
          {
            "matcher": {
              "id": "byName",
              "options": "job"
            },
            "properties": [
              {
                "id": "custom.width",
                "value": 210
              }
            ]
          },
          {
            "matcher": {
              "id": "byName",
              "options": "namespace"
            },
            "properties": [
              {
                "id": "custom.width",
                "value": 190
              }
            ]
          }
        ]
      },
      "gridPos": {
        "h": 16,
        "w": 12,
        "x": 0,
        "y": 11
      },
      "id": 554,
      "options": {
        "footer": {
          "fields": "",
          "reducer": [
            "sum"
          ],
          "show": false
        },
        "showHeader": true,
        "sortBy": [
          {
            "desc": true,
            "displayName": "Replicas"
          }
        ]
      },
      "pluginVersion": "9.0.4",
      "targets": [
        {
          "datasource": {
            "type": "prometheus",
            "uid": "000000003"
          },
          "editorMode": "code",
          "exemplar": false,
          "expr": "kube_deployment_spec_replicas{cluster=~\"$cluster\"}",
          "format": "table",
          "instant": true,
          "range": false,
          "refId": "A"
        }
      ],
      "title": "Deployments Replicas",
      "transformations": [
        {
          "id": "organize",
          "options": {
            "excludeByName": {
              "Time": true,
              "__name__": true,
              "deployment": false,
              "instance": true,
              "job": true
            },
            "indexByName": {},
            "renameByName": {
              "Value": "Replicas"
            }
          }
        }
      ],
      "type": "table"
    },
    {
      "datasource": {
        "type": "prometheus",
        "uid": "000000003"
      },
      "fieldConfig": {
        "defaults": {
          "color": {
            "mode": "thresholds"
          },
          "custom": {
            "align": "auto",
            "displayMode": "color-text",
            "inspect": false
          },
          "mappings": [],
          "thresholds": {
            "mode": "absolute",
            "steps": [
              {
                "color": "green",
                "value": null
              },
              {
                "color": "red",
                "value": 80
              }
            ]
          }
        },
        "overrides": [
          {
            "matcher": {
              "id": "byName",
              "options": "Time"
            },
            "properties": [
              {
                "id": "custom.width",
                "value": 211
              }
            ]
          },
          {
            "matcher": {
              "id": "byName",
              "options": "cluster"
            },
            "properties": [
              {
                "id": "custom.width",
                "value": 275
              }
            ]
          },
          {
            "matcher": {
              "id": "byName",
              "options": "job"
            },
            "properties": [
              {
                "id": "custom.width",
                "value": 210
              }
            ]
          },
          {
            "matcher": {
              "id": "byName",
              "options": "namespace"
            },
            "properties": [
              {
                "id": "custom.width",
                "value": 190
              }
            ]
          }
        ]
      },
      "gridPos": {
        "h": 16,
        "w": 12,
        "x": 12,
        "y": 11
      },
      "id": 557,
      "options": {
        "footer": {
          "fields": "",
          "reducer": [
            "sum"
          ],
          "show": false
        },
        "showHeader": true,
        "sortBy": []
      },
      "pluginVersion": "9.0.4",
      "targets": [
        {
          "datasource": {
            "type": "prometheus",
            "uid": "000000003"
          },
          "editorMode": "code",
          "exemplar": false,
          "expr": "kube_statefulset_status_replicas{cluster=~\"$cluster\"}",
          "format": "table",
          "instant": true,
          "range": false,
          "refId": "A"
        }
      ],
      "title": "Statefulset Replicas",
      "transformations": [
        {
          "id": "organize",
          "options": {
            "excludeByName": {
              "Time": true,
              "__name__": true,
              "deployment": true,
              "instance": true
            },
            "indexByName": {},
            "renameByName": {
              "Value": "Replicas"
            }
          }
        }
      ],
      "type": "table"
    }
  ],
  "refresh": false,
  "schemaVersion": 36,
  "style": "dark",
  "tags": [],
  "templating": {
    "list": [
      {
        "current": {
          "selected": false,
          "text": "e2dev-tanzu-rdm-tkc",
          "value": "e2dev-tanzu-rdm-tkc"
        },
        "datasource": {
          "type": "prometheus",
          "uid": "000000003"
        },
        "definition": "label_values(node_uname_info,cluster)",
        "hide": 0,
        "includeAll": true,
        "label": "Cluster",
        "multi": true,
        "name": "cluster",
        "options": [],
        "query": {
          "query": "label_values(node_uname_info,cluster)",
          "refId": "StandardVariableQuery"
        },
        "refresh": 1,
        "regex": "",
        "skipUrlSync": false,
        "sort": 0,
        "type": "query"
      },
      {
        "current": {
          "selected": false,
          "text": "kubernetes-pods",
          "value": "kubernetes-pods"
        },
        "datasource": {
          "type": "prometheus",
          "uid": "000000003"
        },
        "definition": "label_values(node_uname_info, job)",
        "hide": 2,
        "includeAll": false,
        "multi": false,
        "name": "job",
        "options": [],
        "query": {
          "query": "label_values(node_uname_info, job)",
          "refId": "StandardVariableQuery"
        },
        "refresh": 1,
        "regex": "kubernetes-pods",
        "skipUrlSync": false,
        "sort": 1,
        "type": "query"
      },
      {
        "current": {
          "selected": false,
          "text": "cert-manager",
          "value": "cert-manager"
        },
        "datasource": {
          "type": "prometheus",
          "uid": "000000003"
        },
        "definition": "label_values(kube_pod_info{cluster=~\"$cluster\"}, namespace) ",
        "hide": 0,
        "includeAll": false,
        "label": "Namespace",
        "multi": false,
        "name": "namespace",
        "options": [],
        "query": {
          "query": "label_values(kube_pod_info{cluster=~\"$cluster\"}, namespace) ",
          "refId": "StandardVariableQuery"
        },
        "refresh": 1,
        "regex": "",
        "skipUrlSync": false,
        "sort": 1,
        "type": "query"
      },
      {
        "allValue": "",
        "current": {
          "selected": false,
          "text": "cert-manager-69fc644788-m6rhn",
          "value": "cert-manager-69fc644788-m6rhn"
        },
        "datasource": {
          "type": "prometheus",
          "uid": "000000003"
        },
        "definition": "label_values(kube_pod_info{namespace=~\"$namespace\", cluster=~\"$cluster\", job=~\"kube-state-metrics\",}, pod)",
        "hide": 0,
        "includeAll": false,
        "label": "Pod",
        "multi": false,
        "name": "pod",
        "options": [],
        "query": {
          "query": "label_values(kube_pod_info{namespace=~\"$namespace\", cluster=~\"$cluster\", job=~\"kube-state-metrics\",}, pod)",
          "refId": "StandardVariableQuery"
        },
        "refresh": 2,
        "regex": "",
        "skipUrlSync": false,
        "sort": 1,
        "type": "query"
      },
      {
        "current": {
          "selected": true,
          "text": [
            "All"
          ],
          "value": [
            "$__all"
          ]
        },
        "datasource": {
          "type": "prometheus",
          "uid": "000000003"
        },
        "definition": "label_values(node_uname_info{component=~\"node-exporter\",cluster=~\"$cluster\"}, node)",
        "hide": 0,
        "includeAll": true,
        "label": "Node",
        "multi": true,
        "name": "node",
        "options": [],
        "query": {
          "query": "label_values(node_uname_info{component=~\"node-exporter\",cluster=~\"$cluster\"}, node)",
          "refId": "StandardVariableQuery"
        },
        "refresh": 2,
        "regex": "/.*/",
        "skipUrlSync": false,
        "sort": 1,
        "type": "query"
      }
    ]
  },
  "time": {
    "from": "now-15m",
    "to": "now"
  },
  "timepicker": {},
  "timezone": "",
  "title": "01-K8s Tanzu Cluster Health Overview",
  "uid": "xFyT4ce7k",
  "version": 69,
  "weekStart": ""
}
